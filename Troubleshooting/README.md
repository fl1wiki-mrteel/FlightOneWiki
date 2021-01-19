# Troubleshooting - Main



## Radio setup/wizard

<b>Problem:</b> Radio/Reciever not detected</br>
</br>
You have a Crossfire RX:
- CRSF has a solid (not blinking) green light (If blinking, do a factory reset and bind again)
- Telemetry working
- CRSF ch1 (CRSF TX) connected to TX1 on Flightcontroller
    - Almost all flightcontrollers want you to use UART1 for your reciever, some MatekF411 boards may want you to use UART2.
- UART is uninverted (normal/nor)
    - On RevoltOSD/Millivolt bridge TX1/NOR

<b>Solution:</b></br>
Open FalcoX Configurator and paste the following lines one by one. Then restart your flightcontroller.</br>
This solution will result in your sticks not being calibrated, so not a long term fix.</br>

```
SET uart1_protocol=2
SET uart1_pinswap=1
SET wizard_flags=127
SAVE

```

If this is your initial setup you should do the motor mapping wizard,  "RESET_WIZARD MOTOR".</br>
Open FalcoX Configurator and paste the following lines one by one. Then restart your flightcontroller.
```
RESET_WIZARD MOTOR
```
</br>
...<b>Or </b>if that dont work restore a whole DUMP/Backup-file and restore to factory defaults.
</br>
</br>

<b>Step #1</b></br>
Restore from a backup (Just needs to be a FalcoX backup) [Backup/Dump](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/DUMPS/H7.txt) </br>
copy/paste or use built in function to restore configuration.
</br>
</br>
<b>Step #2</b></br>
Reset to factory defaults:</br>
```
RESET_CONFIG
RESETCONFIG
SAVE

```
<b>Step #3</b></br>
Do the initial setup wizard again thru OSD (Goggles)
</br>
</br>
</br>
### Radio setup/wizard - how to

Edit to match your UART-number, and protocol is found in table below

```
SET uart<number>_protocol=<Array Index>
```

Name | Array Index | Note
----- | ----- | -----
Off | 0 | N/A
Spek DSMX | 1 | N/A
CRSF | 2 | N/A
SBUS | 3 | N/A
FPORT | 4 | N/A
Inverted SBUS | 5 | N/A
Inverted FPORT | 6 | N/A
SUMD | 7 | N/A
IBUS | 8 | N/A
Smart Audio | 9 | N/A
Tramp Telem | 10 | N/A
Blheli Telem | 11 | N/A
SRXL2 | 12 | N/A
DJI | 13 | N/A
MSP | 14 | N/A
GPS | 15 | N/A
FLX LEDS | 16 | N/A
null | 17 | N/A


Edit "pinswap" to match your pad.
- if TX is used as RX eg for reciever (RX), pinswap should be 1
- if RX is used pinswap should be 0

```
SET uart<number>_pinswap=<if tx pad, 1. if rx pad 0>
```

Set setup wizard as completed:
```
SET wizard_flags=127
```


## Radio RSSI

<b>Problem:</b> RSSI stuck at xx% in osd </br>
</br>
<b>Solution:</b></br>
- Double check nothing is sent on Channel 8 from your transmitter/radio.
- If using TBS Crossfire
    - Make sure your RX is sending RSSI, LQ or LQ/RSSI on Ch8

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/CRSF_NANO_CH8.JPG)


## OSD Not working

- Camera and VTX should have common ground
- PAL / NTSC must match camera settings

[How to Enter OSD](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/InitialSetup/OSD.md)


## Enter DFU mode

Using CLI you can write "DFU":

```
DFU
```

If thats not possible you can jumper these pads

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/DFU_Bridge.JPG)



## Enter Bootloader mode

Press the button while powering the Flightcontroller

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/H7_REAL_UP_BUTTON.jpg)




## External links
- [Get Crossfire RSSI in Flightone OSD, easier then you think! - 2dogrc](https://www.youtube.com/watch?v=3qxWdBMQSNU)




 