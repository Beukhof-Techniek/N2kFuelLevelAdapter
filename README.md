# NMEA2000 Fuel Level Adapter

## General
This repository shows how to build an adapter which reads the value (resistance) of a fuel level meter and publishes this information as a NMEA 2000 PGN (see the "NMEA 2000" paragraph below). With some minor modifications this design can be used with different types (brands and therefore values) of level meters and can even be used for water levels. The latter will make use of a different PGN which will be explained further in this document.

## NMEA 2000
NMEA 2000, abbreviated to NMEA2k or N2K and standardised as IEC 61162-3, is a plug-and-play communications standard used for connecting marine sensors and display units within ships and boats. Electrically, NMEA 2000 is compatible with the Controller Area Network ("CAN Bus") used on road vehicles and fuel engines. The higher-level protocol format is based on SAE J1939, with specific messages for the marine environment.
Every message that is communicated, consists of a header and a data packet. The header specifies the transmitting device, the device to which the message was sent (which may be all devices), the message priority and the PGN (Parameter Group Number) which indicates the type of the message and thus how the data bytes should be interpreted.

A few examples of PGNs are:
|PGN|Description|
|----|-----|
|127505|Fluid level|
|127508|Battery status|
|128259|Speed: Water referenced|
|128267|Water depth|

Sources: [NMEA 2000 on Wikipedia](https://en.wikipedia.org/wiki/NMEA_2000) and [NMEA 2000 PGN Information by Garmin](https://www8.garmin.com/manuals/webhelp/gpsmap7400-7600/EN-US/GUID-0C4B3FAB-3E41-438C-B31E-9B5489790913.html)

## Supported message types:
|Message|Description|PGN|
|----|-----|-------|
|1-3|Class A position report|129038|
|5|Class A static and voyage related data|129794|

...
