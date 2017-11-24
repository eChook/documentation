# System Overview

There are three systems to the eChook Data Logging and Telemetry; the Arduino based hardware with sensors on the car to collect the data, an Android app to receive the data, log it to file, display it to the driver and upload it, and a web portal to display the data in real time to the rest of the team.

The PCB design, Arduino code and Android app are open sourced under the MIT liscence. This means that anyone is welcome to copy, modify and use the designs as they like. If a team has an existing data logging system on the car, it is possible to add a bluetooth module to that, connect to the eChook Android app and use the driver display, data logging and online telemetry free of charge.


## eChook nano Board

![](https://lh3.googleusercontent.com/7FLh6EmgoqFBk9Twgt-iS4O559Hd256QkYxNOR44Ojl2a_ssA4CzK5mZhyTLCnsBX6XhAC1IYFK9AWPOva-g4_6PjabCO38x9b5HM0y2MPjtWZUsybBmNco646XR3HOmOY3rDIQhI6QzFgvRTwfHY3f4ILqefgRU7SMkqVYkJehNtMq1w06adJ4Fm_ed0PMgliGXGB09yiJIrBb2sxE6-WbumagtFEnnjxTCSKrMIzWJZL8lphKVgRf7XsHWYOjaXi5ZpQIwB9kZkep0LTyaQ1NtaNaHjJCTFSumcsnoew_8HhzZO04JZwq3aIVhWcz0wHUaYQKMGRDE16yFIiWs5v_THXujNE0GPTq8-ll6LsQ64B2xzGPPLc_wYxpl9B6PwEG_l0JtPFbTa-sINt7yuBCc7SxzdeY1qCXBW1rX98_1sP64lAP3dJ_tSZMtUvjuf5RQ2wPtZC5XO_wUJ3Td45kccnCeSD6RYvgSWONEfL-i_LEpvZJ1BQlovem-s5xgKk4qk_LC7R-g7i8mdI1DReJkR2NkcVQNEhwDUaXtyb44a3slhQAaSSyc9WprRyD5OCocPjRQsE-DMtfk8NChR-wJdg8EQm8CJ7vnbfmBZnMyczb7n_TVQXNfZ6w3VxgvdVdumHdumFNLwIsfPwVQyZl97S2Ap-HUkv_g=w274-h205-no)

The eChook nano board is a custom PCB with interfaces for sensors, an Arduino nano to read the sensors and a bluetooth module to send collected data to the Android app. The board takes power from the +24V car batteries.

The board has been designed using circuits and components covered in the GCSE and A level Electronics Curriculum in the hope that teams can understand the board as much as possible.

The PCB uses through hole components and generous solder pads to aid teams in soldering up the board in the classroom.
