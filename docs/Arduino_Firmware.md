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
