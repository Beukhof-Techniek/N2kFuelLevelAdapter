# NMEA 2000 Fuel Level Adapter

## General
This project shows how to build an adapter which reads the value (resistance) of a fuel level meter and publishes this information as a NMEA 2000 PGN (see the [NMEA 2000](https://github.com/Beukhof-Techniek/N2kFuelLevelAdapter/wiki/NMEA-2000) Wiki page within this project). Due to the complexity and fairly high cost of getting started with a NMEA 2000 network, this project also incorporates an HTML5-based meter display so measured data can be viewed on a WiFi enabled device such as a Mobile Phone. Thus being able to start out with a single (stand-alone) device. With some minor modifications this design can be used with miscellaneous types (brands and therefore values) of level meters and can also be used for reporting other types of fluid levels.

## Features
- Buffered connection to the NMEA 2000 network;
- Support for multiple versions (brands/types/values) of Level Meters;
- WiFi integration with HTML5-based meter display;
- Using the ESP32 platform.

## Supported message types:
|Message|Description|PGN|
|----|-----|-------|
|1-3|Class A position report|129038|
|5|Class A static and voyage related data|129794|

...
