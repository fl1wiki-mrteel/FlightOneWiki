



#'''

function Parse-MultiURL($searchstring){

    #[Microsoft.PowerShell.Commands.PSUserAgent].GetProperties() |
    #Select-Object Name, @{n='UserAgent';e={ [Microsoft.PowerShell.Commands.PSUserAgent]::$($_.Name) }}
    $userAgent = [Microsoft.PowerShell.Commands.PSUserAgent]::Chrome

    $links = iwr https://www.banggood.com/search/$($searchstring).html?from=nav -UserAgent $userAgent
    $ResultLinks = $links.links | ?{ ($_.InnerHTML -like "*AIO*") -and ($_.InnerHTML -like "*F4*")} | select title,href

    $script:Table_results = @()
    $script:Table_results += "Name|Brand name|FalcoX Tested|URL|MCU|MPU/IMU|TARGET|OSD|PRICE"
    $script:Table_results += "-----|-----|-----|-----|-----|-----|-----|-----|-----"

    foreach($link in $ResultLinks){

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

            if(!$Name_){$Name_ = "N/A"}
            if(!$Brand_Name_){$Brand_Name_ = "N/A"}
            if(!$MCU_){$MCU_ = "N/A"}
            if(!$TARGET_){$TARGET_ = "N/A"}
            if(!$OSD_){$OSD_ = "N/A"}

            $script:Table_results += "$($Name_)| $($Brand_Name_)| No | [Link]($($url)) | $($MCU_) | $($MPU_) | $($TARGET_) | $($OSD_) | $($Price)"

        }

        $table = ""
    }

    $Table_results | Out-file "C:\Users\teel\Desktop\FL1Lic.csv" -Encoding utf8

    import-csv "C:\Users\teel\Desktop\FL1Lic.csv" -delimiter "|"


}

Parse-MultiURL -searchstring "AIO Flight Controller"

#'''



#Single url

function Parse-SingleURL($url){

    #[Microsoft.PowerShell.Commands.PSUserAgent].GetProperties() |
    #Select-Object Name, @{n='UserAgent';e={ [Microsoft.PowerShell.Commands.PSUserAgent]::$($_.Name) }}
    $userAgent = [Microsoft.PowerShell.Commands.PSUserAgent]::Chrome

    $script:Table_results = @()
    $script:Table_results += "Name|Brand name|FalcoX Tested|URL|MCU|MPU/IMU|TARGET|OSD|PRICE"
    $script:Table_results += "-----|-----|-----|-----|-----|-----|-----|-----|-----"

        #$url = "https://www.banggood.com/Mamba-F411-AIO-F4-Flight-Controller-25A-4S-Blheli_S-DSHOT600-Brushless-ESC-Stack-comptaible-DJI-FPV-Air-Unit-25_5x25_5mm-for-Whoop-Toothpick-RC-Drone-FPV-Racing-p-1703967.html?cur_warehouse=CN&rmmds=search"

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

            if(!$Name_){$Name_ = "N/A"}
            if(!$Brand_Name_){$Brand_Name_ = "N/A"}
            if(!$MCU_){$MCU_ = "N/A"}
            if(!$TARGET_){$TARGET_ = "N/A"}
            if(!$OSD_){$OSD_ = "N/A"}

            $script:Table_results += "$($Name_)| $($Brand_Name_)| No | [Link]($($url)) | $($MCU_) | $($MPU_) | $($TARGET_) | $($OSD_) | $($Price)"

        }

        $table = ""
    

    $Table_results | Out-file "C:\Users\teel\Desktop\FL1LicSingle.csv" -Encoding utf8
    import-csv "C:\Users\teel\Desktop\FL1LicSingle.csv" -delimiter "|"

}

Parse-SingleURL -url "https://www.banggood.com/25_5+25_5mm-AuroraRC-F411-AIO-F4-Flight-Controller-OSD-30A-2-4S-Blheli_-S-Brushless-ESC-for-RC-Drone-FPV-Racing-p-1667206.html?rmmds=myorder&cur_warehouse=CN"



