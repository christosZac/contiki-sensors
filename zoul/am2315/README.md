# contiki-sensors: AM2315

Contiki I<sup>2</sup>C drivers for the [Zolertia zoul](https://github.com/Zolertia/Resources/wiki/The-Zoul-module) mote. 

##AM2315 temperature & humidity sensor

Datasheet and more information [here](https://www.adafruit.com/product/1293).  
Make sure you follow the voltage requirements and correct wiring!


##set up

1. Copy ```am2315.c``` and ```am2315.h``` to your ```/dev``` directory. Default is ```$CONTIKI_HOME/platform/zoul/dev```.
2. Edit the ```Makefile``` of your   project and add the ```am2315.c``` to the ```CONTIKI_TARGET_SOURCEFILES``` variable.
3. Make sure the ```/dev``` directory is set (if differnet from default).

##example
1. Copy the ```test-am2315.c``` to the ```$CONTIKI_HOME/examples/zolertia/zoul/``` directory.
2. Edit the Makefile, adding the line: 

	```Makefile
	CONTIKI_TARGET_SOURCEFILES += am2315.c
	```
3. Plug in a zoul mote, compile and upload:

	```shell
	make TARGET=zoul test-am2315.upload
	```
4. Open a serial terminal to read the sensor value.


