# ESC

# ESC Protocols

Name | Array value/Index | kHz | Speed | Note
----- | ----- | -----  | -----  | -----
Multishot | 0 | N/A | 5-25 uS | N/A
DSHOT64 | 1 | ~64 kHz | 7 uS | Same as DSHOT2400? requires Blheli_32 F3 ESC
DSHOT32 | 2 | ~32 kHz | 13 uS | Same as DSHOT1200? requires Blheli_32 ESC
DSHOT1200 | 3 | ~32 kHz | 13 uS | requires Blheli_32 ESC
DSHOT600 | 4 | ~16 kHz | 26.7 uS / 600,000 bits/Sec | N/A
DSHOT300 | 5 | ~10,6 kHz | 53.3 uS / 300,000 bits/Sec | N/A
Proshot32 | 6 | ~32 kHz ? | 13 uS ? | N/A
Proshot16 | 7 | ~16 kHz ? | 26.7 uS ? |N/A


# ESC Settings

## ESC BLheli_32 F3 (96kHz) Settings

Name | Value | Note
----- | ----- | -----
Ramp up power | 50% | 25% if desync on 50%
Demag | Low | N/A
Timing | 30 | N/A
PWM Freq | 96kHz | N/A

## ESC BLheli_32 F0 (48kHz) Settings

Name | Value | Note
----- | ----- | -----
Ramp up power | 25% | N/A
Demag | Low | N/A
Timing | 30 | N/A
PWM Freq | 48kHz | N/A

or

Name | Value | Note
----- | ----- | -----
Ramp up power | 12.5% | N/A
Demag | Low | N/A
Timing | 23 | N/A
PWM Freq | 48kHz | N/A

## ESC BLheli_s Settings

Name | Value | Note
----- | ----- | -----
Ramp up power | 25% | N/A
Demag | Low | N/A
Timing | 30 | N/A
PWM Freq | N/A | N/A