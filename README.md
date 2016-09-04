# Install SmingRTOS for ESP8266 in Arch Linux 

Install required software. You can see requered packages here 

Clone esp_open_sdk 
	git clone --recursive https://github.com/pfalcon/esp-open-sdk.git

Add files: 
	Clone this repo
	cp esp-open-sdk_additional_files/*  esp-open-sdk/
	cd esp-open-sdk; unzip ESP8266_RTOS_SDK-v1.3.0.10.zip

Build esp_open_sdk 
	cd esp-open-sdk
	make STANDALONE=y

Get SmingRTOS repository:
	https://github.com/SmingHub/SmingRTOS

Set ESP_HOME and SMING_HOME 
	export ESP_HOME=<yout path>/esp-open-sdk
	export SMING_HOME=<your path>/SmingRTOS/sming

Set SmingRTOS SDK_BASE variable:
	export SDK_BASE=$ESP_HOME/ESP8266_RTOS_SDK-v1.3.0
	OR
	vim $SMING_HOME/ Makefile-linux.mk

https://github.com/kireevco/esp-alt-sdk
https://bintray.com/kireevco/generic/ESP8266_RTOS_SDK#files
https://bintray.com/kireevco/generic/download_file?file_path=ESP8266_RTOS_SDK-v1.3.0.10.zip
https://bintray.com/kireevco/generic/esp-alt-sdk

https://github.com/espressif/ESP8266_RTOS_SDK/

https://github.com/SmingHub/SmingRTOS


