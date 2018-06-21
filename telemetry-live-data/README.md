# Telemetry \(Live Data\)

One of the benefits of using a smartphone to log the data is it’s internet connection. With the exception of some tracks with poor signal, this provides an excellent opportunity to get the logged data back to the rest of the team in near real time..

Ideally this system would be simple to use, free to use and secure - we don’t want to publicly broadcast anyone’s location! While we work out how to implement this properly, we found an interim solution using dweet.io.

eChook has no affiliation with dweet.io, they are simply useful services that we’ve found.

We are in the process of building an in house telemetry system that will be both private and free to use - hopefully this will be up and running for the start of the 2018 season \(We're a bit behind schedule... hang tight!\).

Data available in telemetry:

| **Data** | **Identifier** | **Unit** | **Comment** |
| :--- | :--- | :--- | :--- |
| Total Voltage | Vt | Volts | Combined voltage of both batteries - ~24V expected |
| Lower Battery Voltage | V1 | Volts | Upper battery voltage can be calculated on freeboard by Vt-V1 |
| Current | A | Amps |  |
| Motor RPM | RPM | RPM |  |
| Vehicle Speed | Spd | Meters per second | Multiply by 2.23694 for MPH |
| Throttle | Thrtl | Percent |  |
| Temperature 1 | Tmp1 | °C |  |
| Temperature 2 | Tmp2 | °C |  |
| Amp Hours Used | AH | Amp hours |  |
| Lap Number | Lap | - | Current Lap number as counted by the app. |
| Gear | Gear | - | Current gear as calculated by app |
| Brake Applied | Brk | - | 100 if brake is applied, 0 if not. |
| Longitude | Lon | Degrees | GPS Longitude. \(Not available through dweet.io\) |
| Latitude | Lat | Degrees | GPS Latitude. \(Not available through dweet.io\) |

