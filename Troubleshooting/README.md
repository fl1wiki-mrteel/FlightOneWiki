# Troubleshooting - Main



## Radio setup/wizard

<b>Problem:</b> Radio/Reciever not detected</br>
</br>
You have a Crossfire RX:
- CRSF has a green light
- telemetry working
- CRSF ch1 (CRSF TX) connected to TX1 on Flightcontroller  

<b>Solution:</b>
Open FalcoX Configurator and paste the following lines one by one. Then restart your flightcontroller and adjust the motor directions in OSD menu.
```

SET uart1_protocol=2
SET uart1_pinswap=1
SET wizard_flags=127
SAVE

```

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