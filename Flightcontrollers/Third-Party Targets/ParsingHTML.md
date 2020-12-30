



#'''

#[Microsoft.PowerShell.Commands.PSUserAgent].GetProperties() |
#Select-Object Name, @{n='UserAgent';e={ [Microsoft.PowerShell.Commands.PSUserAgent]::$($_.Name) }}
$userAgent = [Microsoft.PowerShell.Commands.PSUserAgent]::Chrome

$links = iwr https://www.banggood.com/search/aio-flight-controller.html?from=nav -UserAgent $userAgent
$ResultLinks = $links.links | ?{ ($_.InnerHTML -like "*AIO*") -and ($_.InnerHTML -like "*F4*")} | select title,href

$Table_results = @()
$Table_results += "Name|Brand name|MCU|MPU/IMU|TARGET|OSD|PRICE|FalcoX Tested|URL"
$Table_results += "-----|-----|-----|-----|-----|-----|-----|-----|-----"

foreach($link in $ResultLinks){


    #$url = "https://www.banggood.com/Mamba-F411-AIO-F4-Flight-Controller-25A-4S-Blheli_S-DSHOT600-Brushless-ESC-Stack-comptaible-DJI-FPV-Air-Unit-25_5x25_5mm-for-Whoop-Toothpick-RC-Drone-FPV-Racing-p-1703967.html?cur_warehouse=CN&rmmds=search"
    #$url = "https://www.banggood.com/20x20mm-JHEMCU-GHF420AIO-F4-OSD-Flight-Controller-w-or-5V-9V-BEC-and-Current-Sensor-AIO-20A-BL_S-2-6S-4In1-Brushless-ESC-Support-DJI-Air-Unit-for-RC-Drone-FPV-Racing-p-1745432.html?cur_warehouse=CN&amp;rmmds=search"

    $url = $link.href

    $iwr = iwr $url -UserAgent $userAgent
    $result = ($iwr.ParsedHtml.getElementsByTagName('div') | Where{ $_.className -eq 'tab-cnt' } ).innerText
    $Price = ($iwr.ParsedHtml.getElementsByTagName('span') | Where{ $_.className -eq 'main-price' } ).innerText
    $Price

    #Split lines
    $a = $result.Split([Environment]::NewLine)
    
    #Split each line that includes ":"
    $table = New-Object PSObject
    Foreach($contentLine in $a){

        if($contentLine -like "*:*"){
            $table | Add-Member NoteProperty -Name "$($($($contentLine -split ':')[0]).Trim())" -Value "$($($($contentLine -split ':')[1]).Trim())" -ErrorAction silentlycontinue
        }
        
    }
    
    #$table | ft

    #$table | select "Item *", size, "Brand*", "Mounting*", "Dimensions*", "ESC Current", "*MPU*", "*CPU*", MCU, IMU, OSD, TARGET, fw, Firmware | ft

    $Name_ = $table."Item Name"
    $Brand_Name_ = $table."Brand Name"
    $MCU_ = $table | select "*MCU*", "*CPU*" | ?{$_ -like "*STM*"}
    $MPU_ = $table | select "*MPU*", "*IMU*" | ?{ ($_ -like "*MPU*") -or ($_ -like "*IMC*")}
    $TARGET_  = $table | select "*TARGET*", "*FW*", "*Firmware*" | ?{$_ -like "*F411*"}
    $OSD_ = $table.OSD

    if($TARGET_){

        $MCU_ = $MCU_ -replace "@{","" -replace "}",""
        $MPU_ = $MPU_ -replace "@{" -replace "}",""
        $TARGET_ = $TARGET_ -replace "@{" -replace "}",""
        $Table_results += "$($Name_)| $($Brand_Name_)| $($MCU_)| $($MPU_)| $($TARGET_)| $($OSD_)|$($Price) | 'No'| [Link]($($url))"

    }


    $table = ""
}

$Table_results | Out-file "C:\Users\teel\Desktop\FL1Lic.csv" -Encoding utf8

import-csv "C:\Users\teel\Desktop\FL1Lic.csv" -delimiter "|"

#'''