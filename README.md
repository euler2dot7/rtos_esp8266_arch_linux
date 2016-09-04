# Install SmingRTOS for ESP8266 in Arch Linux 

### this repo based on  https://github.com/SmingHub/Sming/wiki/Linux-Quickstart 

## Install required software: 
You can see requered packages here  https://github.com/SmingHub/Sming/wiki/Linux-Quickstart

## Clone esp_open_sdk 
	```shell
	git clone --recursive https://github.com/pfalcon/esp-open-sdk.git
	```

## Add files: 
	Clone this repo and copy filese to esp-open-sdk dir
	```shell
	cp esp-open-sdk_additional_files/*  esp-open-sdk/
	cd esp-open-sdk; unzip ESP8266_RTOS_SDK-v1.3.0.10.zip
	```

## Build esp_open_sdk 
	```shell
	cd esp-open-sdk
	make STANDALONE=y
	```

## Get SmingRTOS repository:
	```shell
	https://github.com/SmingHub/SmingRTOS
	```

## Set env variables: 
	```shell
	export ESP_HOME=<yout path>/esp-open-sdk
	export SMING_HOME=<your path>/SmingRTOS/sming
	```

## Set SmingRTOS SDK_BASE variable:
	```shell
	export SDK_BASE=$ESP_HOME/ESP8266_RTOS_SDK-v1.3.0
	```
	OR
	```shell
	vim $SMING_HOME/ Makefile-linux.mk
	```
## Build sming:
	```shell
	cd  $SMING_HOME
	make
	cd spiffy
	make
	```

## Verify:
	```shell
	cd $SMING_HOME/../samples/Basic_Blink/
	make 
	make flashinit
	make flash
	```

## Eclipse integration 
	https://github.com/SmingHub/Sming/wiki/Windows---Manual-Installation#eclipse-ide-variables

## Useful links
https://github.com/kireevco/esp-alt-sdk
https://bintray.com/kireevco/generic/ESP8266_RTOS_SDK#files
https://bintray.com/kireevco/generic/download_file?file_path=ESP8266_RTOS_SDK-v1.3.0.10.zip
https://bintray.com/kireevco/generic/esp-alt-sdk

https://github.com/espressif/ESP8266_RTOS_SDK/

https://github.com/SmingHub/SmingRTOS


