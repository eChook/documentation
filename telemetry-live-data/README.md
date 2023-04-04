# Telemetry (Live Data)

One of the benefits of using a smartphone to log the data is it’s internet connection. With the exception of some tracks with poor signal, this provides an excellent opportunity to get the logged data back to the rest of the team in near real time.

The app provides three different ways to send data out.

### eChook Private Live Data

This is our own in house system available at [data.echook.uk](https://data.echook.uk). Each car has a login, only people with that login can see your data. This is a free service provided by eChook to anyone using the app - it can also be used with custom hardware so long as it sends the correct data to the app (See [Bluetooth Communication](../bluetooth-communication/) section).

### dweet.io

This is a free, publicly available service for sending data over the internet, but there is no privacy, anyone with your ID code (or 'Thing Name') can see your data. This does allow some nice features such as FreeBoard or Node Red Integration.

### Custom URL

You can enter a URL, username and password into the app and it will send data to your server in the format of:

```
https://username:password@example.com/../{Stringified JSON}
```

### Data available in telemetry:

| **Data**              | **Identifier** | **Unit**          | **Comment**                                                   |
| --------------------- | -------------- | ----------------- | ------------------------------------------------------------- |
| Total Voltage         | Vt             | Volts             | Combined voltage of both batteries - \~24V expected           |
| Lower Battery Voltage | V1             | Volts             | Upper battery voltage can be calculated on freeboard by Vt-V1 |
| Current               | A              | Amps              |                                                               |
| Motor RPM             | RPM            | RPM               |                                                               |
| Vehicle Speed         | Spd            | Meters per second | Multiply by 2.23694 for MPH                                   |
| Throttle              | Thrtl          | Percent           |                                                               |
| Temperature 1         | Tmp1           | °C                |                                                               |
| Temperature 2         | Tmp2           | °C                |                                                               |
| Amp Hours Used        | AH             | Amp hours         |                                                               |
| Lap Number            | Lap            | -                 | Current Lap number as counted by the app.                     |
| Gear                  | Gear           | -                 | Current gear as calculated by app                             |
| Brake Applied         | Brk            | -                 | 100 if brake is applied, 0 if not.                            |
| Longitude             | Lon            | Degrees           | GPS Longitude. (Not available through dweet.io)               |
| Latitude              | Lat            | Degrees           | GPS Latitude. (Not available through dweet.io)                |
