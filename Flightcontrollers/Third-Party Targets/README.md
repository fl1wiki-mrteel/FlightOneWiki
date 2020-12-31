# Third-Party Targets

## Third-Party Targets

MAMBAF411 FL1 License

- Target: MAMBAF411
- MCU: STM32F411CEU6
- IMU: MPU6000
- OSD: AT7456E

MATEKF411 FL1 License 

- Target: MATEKF411
- MCU: STM32F411
- IMU: MPU6000
- OSD: AT7456E


## Flashing firmware
1. Download and install latest FalcoX configurator
    1. [FalcoX Configurator (Alpha)](https://flightone.com/download.php?version=alpha)
    1. [FalcoX Configurator (Beta)](https://flightone.com/download.php?version=beta)    
    1. [FalcoX Configurator (Stable)](https://flightone.com/download.php?version=stable) 
1. Connect your Third-Party Target Flightcontroller
    1. Look at the top left corner, copy the "Serialnumber"
    ![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/ThirdpartytargetConfigurator.JPG)
1. Browse to [Buy Third Party Target Lic page](https://shop.flightone.com/?cat=digital-download&s=&post_type=product)
    1. Select your Firmware target and add it to your shopping cart
    1. Before checkout, add your serial number under "Order notes (optional)"
    ![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/Thirdpartytargetorder.JPG)

    





## Available Third-Party Boards

Name|Brand name|FalcoX Tested|URL|MCU|MPU/IMU|TARGET|OSD|PRICE
-----|-----|-----|-----|-----|-----|-----|-----|-----
HAKRC F411 20A AIO| N/A| No | [Link](https://www.banggood.com/HAKRC-F411-20A-AIO-26mm-Support-PWM-Multishot-Oneshot-DSHOT-7g-w-or-barometer-for-Toothpick-FPV-Racing-RC-Drone-p-1711816.html?rmmds=stop_sale_viewalsoview&cur_warehouse=CN) | *MCU*=; CPU=STM32F411CEU6 | *MPU*=; IMU=MPU6000 | *TARGET*=; *FW*=; Firmware=betaflight_4.1.1_MATEKF411 | AT7456E | US$00.00
N/A| AuroraRC| Yes | [Link](https://www.banggood.com/25_5+25_5mm-AuroraRC-F411-AIO-F4-Flight-Controller-OSD-30A-2-4S-Blheli_-S-Brushless-ESC-for-RC-Drone-FPV-Racing-p-1667206.html?rmmds=myorder&cur_warehouse=CN) | MCU=STM32F411; *CPU*= | *MPU*=; IMU=MPU6000 gyro/accelerometer (SPI) | FC Firmware target=MATEKF411; Target=G_H_30; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
N/A| Geprc| No | [Link](https://www.banggood.com/25_5x25_5mm-GEPRC-GEP-12A-F4-V1_1-F411-F4-Flight-Controller-AIO-OSD-BEC-Current-Sensor-and-12A-BL_S-2-4S-4In1-ESC-for-RC-Drone-FPV-Racing-p-1474473.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; ESC MCU=BB21F16G; *CPU*= | *MPU*=; IMU=MPU6000 gyro/accelerometer (SPI) | Firmware target=MATEKF411; Target=G_H_30; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
F4 Flight Controller Built-in 20A BL_S ESC & Frsky Receiver| Happymodel| No | [Link](https://www.banggood.com/25_5x25_5mm-Happymodel-CrazyF411-AIO-F4-2-4S-Flight-Controller-Built-in-20A-BL_S-ESC-and-Frsky-Receiver-for-Toothpick-RC-Drone-FPV-Racing-p-1764273.html?cur_warehouse=CN&amp;rmmds=search) | F4 Flight ControllerMCU=STM32F411CEU6 (100MHZ, 512K FLASH); *CPU*= | *MPU*=; *IMU*= | Firmware target=MATEKF411RX; *FW*=; Factory firmware=F_H_40_REV16_7.HEX | N/A | US$00.00
Mamba F411 AIO| Mamba| YES | [Link](https://www.banggood.com/Mamba-F411-AIO-F4-Flight-Controller-25A-4S-Blheli_S-DSHOT600-Brushless-ESC-Stack-comptaible-DJI-FPV-Air-Unit-25_5x25_5mm-for-Whoop-Toothpick-RC-Drone-FPV-Racing-p-1703967.html?cur_warehouse=CN&amp;rmmds=search) | MCU=100MHz STM32F411CEU6; *CPU*= | *MPU*=; IMU=MPU6000 | Target=MAMBAF411; *FW*=; Firmware=Betaflight | AT7456E | US$00.00
Betaflight F4 Flight Controller| N/A| No | [Link](https://www.banggood.com/20x20mm-Upgrade-Betaflight-F4-Noxe-V1-Flight-Controller-AIO-OSD-5V-8V-BEC-w-or-Barometer-and-Blackbox-for-RC-Drone-FPV-Racing-p-1310419.html?cur_warehouse=CN&amp;ID=517535&amp;rmmds=search) | *MCU*=; CPU=STM32F411C | MPU=MPU6000; *IMU*= | *TARGET*=; *FW*=; Firmware=betaflight_4.1.0_FLYWOOF411.hex | N/A | US$00.00
99mm Wheelbase F4 2-4S Whoop FPV Racing Drone| FUS| No | [Link](https://www.banggood.com/FUS-Spartan-V3-99mm-Wheelbase-F411-F4-Flight-Controller-AIO-20A-ESC-3-4S-Freestyle-FPV-Racing-Drone-PNP-w-or-200mW-VTX-Runcam-Nano-2-FPV-Camera-p-1723138.html?cur_warehouse=CN&amp;ID=6287830&amp;rmmds=search) | MCU=STM32F411; *CPU*= | *MPU*=; *IMU*= | Target=MATEK F411; *FW*=; ESC Firmware=G_H_30 BLS | N/A | US$00.00
GHF13 AIO F4 OSD Flight Controller Built-in 13A 4In1 ESC| N/A| No | [Link](https://www.banggood.com/16x16mm-JHEMCU-GHF13-AIO-F4-OSD-Flight-Controller-Built-in-13A-Blheli_S-2-4S-4-In-1-Brushless-ESC-for-RC-Drone-FPV-Racing-p-1782009.html?cur_warehouse=CN&amp;rmmds=search) | *MCU*=; CPU=STM32F411CE (100MHZ) | MPU=MPU6000 (SPI); *IMU*= | *TARGET*=; *FW*=; Firmware=Betaflight MATEKF411.HEX; ESC Firmware=BLHELI_S G-H-30.HEX | N/A | US$00.00
F4 Flight Controller AIO 20A BL_S 4In1 ESC| iFlight| No | [Link](https://www.banggood.com/25_5x25_5mm-iFlight-SucceX-D-Whoop-F4-V2-Flight-Controller-w-or-5V-10V-BEC-Output-AIO-20A-BL_S-4in1-2-5S-Brushless-ESC-Support-DJI-Air-Unit-Pulg-and-Play-for-Whoop-Toothpick-FPV-Racing-Drone-p-1709071.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; *CPU*= | *MPU*=; *IMU*= | Target=IFLIGHT_F411_PRO; *FW*=; ESC Firmware=G-H-30 BLS | N/A | US$00.00
N/A| N/A| No | [Link](https://www.banggood.com/GEPRC-GEP-20A-F4-AIO-F4-MPU6000-Flight-Controller-OSD-20A-Blheli_S-2-4S-Brushless-ESC-26_526_5mm-for-Rocket-Lite-3-5-Inch-Cinewhoop-Toothpick-FPV-Racing-Drone-p-1607659.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; ESC MCU=BB21F16G; *CPU*= | *MPU*=; IMU=MPU6000 gy ro/accelerometer (SPI) | FC Firmware target=MATEKF411; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
F4120 AIO 35A| N/A| No | [Link](https://www.banggood.com/20+20mm-HAKRC-F4120-3-6S-35A-AIO-Flight-ControllerandESC-Baro-Version-Compatibled-with-DJI-Air-Unit-p-1759477.html?cur_warehouse=CN&amp;rmmds=search) | *MCU*=; CPU=STM32F411CEU6 | *MPU*=; IMU=MPU6000 | *TARGET*=; *FW*=; Firmware version=betaflight_4.1.1_MATEKF411; Firmware support=BLHELI_ S | AT7456E | US$00.00
AIO F4 Flight Controller 12A 2-4S ESC Frsky Receiver Board| Eachine| No | [Link](https://www.banggood.com/Eachine-AIO-F4-Flight-Controller-12A-2-4S-ESC-Frsky-Receiver-Part-for-Novice-III-Viswhoop-FPV-Racing-Drone-p-1649353.html?cur_warehouse=CN&amp;rmmds=search) | Flight controllerMCU=STM32F411CEU6 (100MHZ, 512K FLASH); *CPU*= | *MPU*=; *IMU*= | Firmware target=MATEKF411RX; *FW*=; Factory firmware=F_H_40_REV16_7.HEX | N/A | US$00.00
F411 F4 Flight Controller AIO OSD BEC Built-in 12A 2-4S 4in1 ESC| AuroraRC| YES | [Link](https://www.banggood.com/AuroraRC-Supra-F4-12A-V1_0-F411-F4-Flight-Controller-AIO-OSD-BEC-Built-in-12A-2-4S-4in1-ESC-for-RC-Drone-p-1520206.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; ESC MCU=BB21F16G; *CPU*= | *MPU*=; IMU=MPU6000 gyroscope/accelerometer (SPI) | Firmware target=MATEKF411; Target=G_H_30; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
F4 Flight Controller AIO OSD BEC| Geprc| No | [Link](https://www.banggood.com/16x16mm-Geprc-Stable-F411-Stack-Part-F4-Flight-Controller-AIO-OSD-BEC-for-RC-Drone-FPV-Racing-p-1564456.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; *CPU*= | *MPU*=; IMU=MPU6000 gyro/accelerometer (SPI) | Firmware target=MATEKF411; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
N/A| N/A| No | [Link](https://www.banggood.com/FLYWOO-GOKU-GN413S-F411-F4-Flight-Controller-AIO-OSD-BEC-and-13A-BL_S-2-4S-4In1-ESC-25_5+25_5mm-for-Toothpick-RC-Drone-FPV-Racing-p-1618411.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; ESC MCU=BB21F16G; *CPU*= | *MPU*=; IMU=MPU6000 gyro/accelerometer (SPI) | Firmware target=FLYWOOF411; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
N/A| FLYWOO| No | [Link](https://www.banggood.com/25_5x25_5mm-FLYWOO-GOKU-GN413S-Stack-AIO-2-4S-F4-Flight-Controller-13A-ESC-VTX625-25-or-50-or-100-or-200-or-450mW-Switchable-for-Toothpick-FPV-Racing-Drone-p-1697083.html?cur_warehouse=CN&amp;rmmds=search) | MCU=STM32F411; ESC MCU=BB21F16G; *CPU*= | *MPU*=; IMU=MPU6000 gyro/accelerometer (SPI) | Firmware target=FLYWOOF411; *FW*= | BetaFlight OSD w/ AT7456E chip | US$00.00
