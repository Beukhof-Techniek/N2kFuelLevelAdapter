# NMEA2000 Fuel Level Adapter

**GENERAL**
This repository shows how to build an adapter which reads the value (resistance) of a fuel level meter and publishes this information as a NMEA2000 PGN. With some minor modifications this design can be used with different types (brands and therefore values) of level meters and can even be used for water levels. The latter will make use of a different PGN which will be explained further in this document.

**Supported message types:**
- 1-3:  Class A position report -> PGN 129038;
- 5:    Class A static and voyage related data -> PGN 129794;
- 14:   Safety related broadcast message -> PGN 129802. This is needed for AIS SART devices!;
- 18:   Class B standard position report -> PGN 129039;
- 19:   Class B extended position report -> PGN 129040;
- 24A:  Class B static data part A -> PGN 129809;
- 24B:  Class B static data part B -> PGN 129810.

...
