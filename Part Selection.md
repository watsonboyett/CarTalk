
# CarTalk
------------

## Goals

* Collect CAN data from car's OBD port
** Sample continuous data at ~1Hz
** Could also have separate "on change" event storage
* Log data to local storage and remove old data
** Save data as CSV (or something human readable) to files on SD card
** Remove files older than 30 days (or some sane limit)
* Save car's telemetry data to remote database (probably InfluxDB)
** Could transmit data in near real-time using cell modem
** Could transmit over WiFi (automatically when returning home)
** Could connect to phone over bluetooth and transmit using phone service
* May need to add shut-down circuitry or battery to hardware to prevent draining car battery
* Analyze car telemetry using GIS and similar tools
** Need to add GPS components to provide geo-position info


## Part Selection

### CAN Interface

* Macchina M2

### IMU (acceleration, gyroscope, magnetometer)

* MPU-9250 ($11, I2C/SPI, 24QFN, Temp Sensor, Motion Processor, 3mm x 3mm)
* LSM9DS1TR ($7, I2C/SPI, 24LGA, Temp Sensor)
* BMX055 ($8, I2C/SPI, 20LGA)

### GPS Receiver

* MAX-M8Q-0 ($30, All Geo Protocols, UART Output, 11mm x 10mm)
* NEO-M8N-0 ($35, All Geo Protocols, UART/SPI/USB Output, 16mm x 12mm )
* M10478-A2-1 ($18, GPS Only, UART Output, 14mm x 10mm)

### Cell Modem

* NL-SW-LTE-TSVG ($130, includes GPS module)
* SARA-G350-02S ($22, GSM/GPRS)
* SARA-U201 ($49, HSPA)

### WiFi (instead of Cell Modem for v1?)

* ESP8266-12S module ($7, on-board antenna)

### LiPo charging

*

