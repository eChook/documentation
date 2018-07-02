# System Overview

There are three systems to the eChook Data Logging and Telemetry; the Arduino based hardware with sensors on the car to collect the data, an Android app to receive the data, log it to file, display it to the driver and upload it, and a web portal to display the data in real time to the rest of the team.

The decision to split the system up like this was primarily cost based. Once you start adding an SD card slot and SD card, GPS receiver, screen etc. to the hardware on the car, costs rise rapidly - but we all carry devices with memory, a screen, GPS and so much more in our pocket every day. By offloading as much of the functionality to the smartphone as possible we have been able to create far simpler and lower cost hardware.

The PCB design, Arduino code and Android app are open sourced under the MIT liscence. This means that anyone is welcome to copy, modify and use the designs as they like. If a team has an existing data logging system on the car, it is possible to add a bluetooth module to that, connect to the eChook Android app and use the driver display, data logging and online telemetry free of charge.

## eChook nano Board

![](https://lh3.googleusercontent.com/7FLh6EmgoqFBk9Twgt-iS4O559Hd256QkYxNOR44Ojl2a_ssA4CzK5mZhyTLCnsBX6XhAC1IYFK9AWPOva-g4_6PjabCO38x9b5HM0y2MPjtWZUsybBmNco646XR3HOmOY3rDIQhI6QzFgvRTwfHY3f4ILqefgRU7SMkqVYkJehNtMq1w06adJ4Fm_ed0PMgliGXGB09yiJIrBb2sxE6-WbumagtFEnnjxTCSKrMIzWJZL8lphKVgRf7XsHWYOjaXi5ZpQIwB9kZkep0LTyaQ1NtaNaHjJCTFSumcsnoew_8HhzZO04JZwq3aIVhWcz0wHUaYQKMGRDE16yFIiWs5v_THXujNE0GPTq8-ll6LsQ64B2xzGPPLc_wYxpl9B6PwEG_l0JtPFbTa-sINt7yuBCc7SxzdeY1qCXBW1rX98_1sP64lAP3dJ_tSZMtUvjuf5RQ2wPtZC5XO_wUJ3Td45kccnCeSD6RYvgSWONEfL-i_LEpvZJ1BQlovem-s5xgKk4qk_LC7R-g7i8mdI1DReJkR2NkcVQNEhwDUaXtyb44a3slhQAaSSyc9WprRyD5OCocPjRQsE-DMtfk8NChR-wJdg8EQm8CJ7vnbfmBZnMyczb7n_TVQXNfZ6w3VxgvdVdumHdumFNLwIsfPwVQyZl97S2Ap-HUkv_g=w274-h205-no)

### Hardware

The eChook nano board is a custom PCB with interfaces for sensors, an Arduino nano to read the sensors and a Bluetooth module to send collected data to the Android app. The board takes power from the +24V car batteries.

The board has been designed using circuits and components covered in the GCSE and A level Electronics Curriculum in the hope that teams can understand the board as much as possible. The PCB also uses through-hole components and generous solder pads to aid teams in soldering up the board in the classroom.

The PCB and circuit designs are available at [github.com/eChook](https://github.com/echook/echook-nano-pcb). You will need [RS DesignSpark PCB](https://www.rs-online.com/designspark/pcb-software) to open and edit these files. It is free for everyone to use.

### Software

The heart of the eChook nano board is the Arduino. The Arduino platform was chosen due to its massive online following, meaning a large community and loads of support available. While C/C++ coding is often not covered in the UK curriculum, the online support makes the Arduino easy to get started with.

The code for the Arduino Nano on the eChook board is available from [github.com/eChook](https://github.com/echook/echook-arduino-nano). It has been written in a step-by-step fashion and commented every step of the way to explain what each bit of code is doing.

## Android App

The eChook Companion app is available for Android devices and can be installed from the [Google Play Store](https://play.google.com/store/apps/details?id=com.ben.drivenbluetooth). As this is also open source, the code for the app can be found on [Github.com/eChook](https://github.com/echook/echook-arduino-android)

The app connects to the Bluetooth module on the eChook nano board and logs the incoming data. It also augments this data with sensors on the phone - primarily GPS location. The app can also use the GPS to count laps, which is added to the logged data. At the end of the session, there is the option to send a .csv data file through the standard Android sharing system, making it easy to add it to Google Drive or Dropbox, email it to someone, or send it using whichever app you choose.

Finally, if the phone has a data connection, the app can upload data in real time to the internet for telemetry.

## Website

The website displays data uploaded from the phone in near realtime. Currently this is to a third party service called [dweet.io](http://dweet.io) which displays the data nicely, but also makes it public. As such, no location information is available.

The data.echook.uk website is under development and will be offered to teams for Beta testing shortly. At first this will be limited to the same real time display functionality of the dweet website, with storage and viewing of historical data to be added at a later point.

