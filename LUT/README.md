# FalcoX Lookup tables
These tables are used to illustrate/map the features array index value.
for e.g. while parsing backup/dump file.

```Powershell

Function Get-FalcoXEscProto($Protocol){
    switch ($Protocol)
    {
        0 { $result = 'Multishot' }
        1 { $result = 'DSHOT64' }
        2 { $result = 'DSHOT32' }
        3 { $result = 'DSHOT1200' }
        4 { $result = 'DSHOT600' }
        5 { $result = 'Dshot8' }
        6 { $result = 'Proshot32' }
        7 { $result = 'Proshot16' }
        Multishot { $result = 0 }
        DSHOT64 { $result = 1 }
        DSHOT32 { $result = 2 }
        DSHOT1200 { $result = 3 }
        DSHOT600 { $result = 4 }
        Dshot8 { $result = 5 }
        Proshot32 { $result = 6 }
        Proshot16 { $result = 7 }
    }

    $result
}

Get-FalcoXEscProto -Protocol 0
#Result: Multishot
Get-FalcoXEscProto -Protocol Multishot
#Result: 0

```

## ESC Protocols

Configuration example, sets esc protocol to DSHOT8:
```
SET esc_protocol=5
```

Name | Array Index | Note
----- | ----- | -----
Multishot | 0 | N/A
Dshot64 | 1 | N/A
Dshot32 | 2 | N/A
Dshot16 | 3 | N/A
Dshot600 | 4 | N/A
Dshot8 | 5 | N/A
Proshot32 | 6 | N/A
Proshot16 | 7 | N/A

## Serial Protocol

Configuration example, sets UART #1 to "off":
```
SET uart1_protocol=0
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

## Filter

Configuration example, sets filter #1 type to "FakeKalman":
```
SET filt1_type=6
```

Name | Array Index | Note
----- | ----- | -----
Predict | 0 | N/A
Biquad | 1 | N/A
Frequency | 2 | N/A
Dynamic | 3 | N/A
Disabled | 4 | N/A
Fir2 | 5 | N/A
FakeKalman | 6 | N/A
BrickWall | 7 | N/A

## RC Filter (RC Smooth)

Configuration example, sets RC Smooth type to "none":
```
SET rc_smoothing_type=0
```

Name | Array Index | Note
----- | ----- | -----
None | 0 | N/A
New | 1 | N/A
Filter | 2 | N/A
old | 3 | N/A

## Filter AA Strenght

Configuration example, sets AA Strength (Gyro) to "off" and D-term AA Strength to "off":
```
SET aa_strength=0
SET d_term_aa_strength=0
```

Name | Array Index | Note
----- | ----- | -----
Off | 0 | N/A
Low | 1 | N/A
Medium | 2 | N/A
Med High | 3 | N/A
High | 4 | N/A
Ultra High | 5 | N/A

## Quopa strenght

Configuration example, sets Quopa strength to "Medium":
```
SET auto_quopa_strength=1
```

Name | Array Index | Note
----- | ----- | -----
Low | 0 | N/A
Med | 1 | N/A
High | 2 | N/A









