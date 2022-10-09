## MobiFlight and Arduino

### Burning Firmware Using Arduino IDE 1.8.19

Downloaded the firmware from https://github.com/MobiFlight/MobiFlight-Connector/releases/. After installing Arduino IDE 1.8.19, burnt the firmware HEX using the installed `avrdude`:

```
C:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude -CC:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf -v -patmega328p -carduino -PCOM3 -b57600 -D -Uflash:w:C:\Users\oodis\Downloads\mobiflight_uno_2_2_0.hex:i 
```

### Burning Firmware Using Arduino IDE 2.0.0

Downloaded the firmware from https://github.com/MobiFlight/MobiFlight-Connector/releases/. After installing Arduino IDE 1.8.19, burnt the firmware HEX using the installed `avrdude`:

```
"C:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude" "-CC:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega328p -carduino "-PCOM4" -b57600 -D "-Uflash:w:C:\Users\oodis\Downloads\mobiflight_uno_2_2_2.hex:i" 
```

### Old Arduino Nano Clones

Experimenting with some old Nano clones in Arduino IDE I had to set the IDE to use the "Old Bootloader". Upon board selection I had to go to "Tools > Processor > ATmega328P (Old Bootloader)" to have the board properly recognized by the Arduino IDE. Was able to upload a generic blink sketch. With Verbose logging turned on, the `avrdude` command was obtained that burns the HEX file. Just needed to modify the path to the HEX file.

### Arduino Uno to Nano PIN Comparison

| ATmega | Uno      | Nano     |
| ------ | -------- | -------- |
|  1     | D3       | D3       |
|  2     | D4       | D4       |
|  9     | D5       | D5       |
|  10    | D6       | D6       |
|  11    | D7       | D7       |
|  12    | D8       | D8       |
|  13    | D9       | D9       |
|  14    | SS       | D10      |
|  15    | D11/MOSI | D11/MOSI |
|  16    | D12/MISO | D12/MISO |
|  17    | D13/SCK/LED | D13/SCK/LED |
|  23    | A0       | A0       |
|  24    | A1       | A1       |
|  25    | A2       | A2       |
|  26    | A3       | A3       |
|  27    | A4/SDA   | A4       |
|  28    | A5/SCL   | A5       |
|  30    | D0/RX    | D0/RX    |
|  31    | D1/TX    | D1/TX    |
|  32    | D2       | D2       |
