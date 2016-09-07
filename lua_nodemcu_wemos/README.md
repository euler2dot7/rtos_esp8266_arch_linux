#Install lua interpreter on nodemcu or wemos board.

### Flash firmware
```shell
./esptool.py --port /dev/ttyUSB0 write_flash -fm qio -fs 32m  0x00000 nodemcu-master-13-modules-2016-09-05-14-04-20-integer.bin 0x3fc000 esp_init_data_default.bin

```
 https://nodemcu.readthedocs.io/en/master/en/flash/

### Nodemcu cloud build 
https://nodemcu-build.com/

### Official documentation
https://nodemcu.readthedocs.io/en/master/

### Eclipse integration 
https://github.com/prikril/ldt-nodemcu

### IDE for lua firmware
http://esp8266.ru/esplorer/

