## MobiFlight and Arduino

### Burning Firmware Using Arduino IDE 1.8.19

After installing Arduino IDE 1.8.19, burnt the firmware HEX using the installed `avrdude`:

```
C:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude -CC:\Users\oodis\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf -v -patmega328p -carduino -PCOM3 -b57600 -D -Uflash:w:C:\Users\oodis\Downloads\mobiflight_uno_2_2_0.hex:i 
```
