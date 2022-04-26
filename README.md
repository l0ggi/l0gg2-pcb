# l0gg2-pcb
2nd gen PCB for l0ggi project

## Project
The idea behind l0ggi is to develop an open source hardware platform to log data, mainly environmental values like temperature and humidity, further also atmospheric pressure, co2, nox etc.
After a quick and dirty pcb with l0gg1 (not working out of the box) the logg2 pcb fixes all bugs of the older iteration and implements the possibility to operate the pcb via battery and accus.
l0gg2 does not feature a usb interface and is designed to be used with the open source tasmota sensors firmware (https://tasmota.github.io/docs/). As the firmware offers the possibility for OTA updates out of the box the usb interface was removed.
The type-c connector of the older iteration is replaced with a overall cheaper micro-usb. The data-lines are not terminated and not used. 

## Ordering
The gerber files are available and proven to work. 
Pick and place files are still in progress

## Firmware
While Tasmota works, the Bosch BME temperature, humidity and atmospheric pressure sensor which is intended to used with the pcb works with Tasmota-Sensors. 

### Flashing
A standard 3.3V FTDI cable can be used, but TX/RX needs to be inverted on the cable. This bug is known and will be fixed in l0gg2.1
Connect USB for power and the adapted FTDI cable to l0gg2. Press PRG (below ESP on the right) and hold and trigger RESET (below ESP on the left). Hold PRG and start flashing via the web tool of tasmota. 

### Configuration (Bosch Sensor, default)
Port | Function
---|---
GPIO0|Button 1
GPIO1|Serial TX
GPIO2|I2C SDA
GPIO3|Serial RX
GPIO4|Button 2
GPIO5|Button 3
GPIO6|
GPIO7|
GPIO8|
GPIO9|
GPIO10|
GPIO11|
GPIO12|
GPIO13|
GPIO14|I2C SCL
GPIO15|
GPIO16|
GPIO17|ADC In

### Configuration (AM2301, soldered to I2C header)
Port | Function
---|---
GPIO0|
GPIO1|
GPIO2|AM2301
GPIO3|
GPIO4|
GPIO5|
GPIO6|
GPIO7|
GPIO8|
GPIO9|
GPIO10|
GPIO11|
GPIO12|
GPIO13|
GPIO14|
GPIO15|
GPIO16|
GPIO17|
