# Temperature

These are the most involved sensors to calibrate, primarily due to the response of the thermistors being non-linear. A typical 10kΩ thermistor resistance vs temperature graph is shown below:

- **V2 Arduino code (code version 2.0 or later):** enter the calculated calibration coefficients in the calibration web app at [configure.echook.uk](https://configure.echook.uk).
- **Legacy Arduino code (below version 2.0):** enter these values in the `calibration.h` file and re-upload the code.

![](https://lh4.googleusercontent.com/z8hZ8SvbFAUlVafoLBIffR0ba-W5_rT01rHz17n3Jz-88D0F088MpPB4ndDL4eUz13awJpIQm42ru8HbgTlM9KoGhY0lbiR4WjP_GLsFwfe0UgLFJYWsLyTQnudFe_yAKh3eBetC)

Note that the 10k refers to the resistance at room temperature \(25°\), and that the resistance decreases as temperature increases. This is called a negative temperature coefficient, or NTC. The eChook board uses a 10k NTC thermistor.

On the board, the thermistor completes the lower half of a potential divider circuit with a 10kΩ resistor, so the voltage at the output of the potential divider falls as the temperature of the thermistor increases.

To translate this voltage to a temperature, the resistance curve of the specific thermistor being used is needed. Due to tolerances, this is subtly different even between identical thermistors. To do this the eChook uses the [Steinhart-Hart](https://en.wikipedia.org/wiki/Steinhart%E2%80%93Hart_equation) equation, which uses three coefficients calculated from the thermistor to convert the resistance seen to an accurate temperature reading.

Use this process:

1. Take three measurements of thermistor resistance at different known temperatures.
2. Open the online calculator [here](https://www.thinksrs.com/downloads/programs/therm%20calc/ntccalibrator/ntccalculator.html).
3. Enter your three temperature/resistance points.
4. Copy the calculated A, B, and C coefficients.
5. For legacy code versions, enter the coefficients in `calibration.h` and re-upload.
6. For V2 code versions, enter the same coefficients in the web app.

The calculator looks like this:

![](https://lh3.googleusercontent.com/fmYhUC_dDDkDMKbMWPzaOq1qHJJ6kehtJjfd_UuTrWpTaNHCxvm0np7ymCy6kjwasyXHZBpfv9XZsvGpLbHzfyuvvEAgYeeR0o73np7Ed0G2BduqZFHUd_0shGBJHHU87K6xzmo4)

For legacy code versions, enter the three temperature and resistance measurements and copy the A, B and C coefficients from the calculator into the `calibration.h` file.

```text
//Board and Sensor Specific Calibrations
const float CAL_THERM_A = 0.001871300068; //Steinhart-Hart constants - See documentation for calibration method
const float CAL_THERM_B = 0.00009436080271;
const float CAL_THERM_C = 0.0000007954800125;
```

To get the default calibration we used a pan of water, digital thermometer, and a multimeter. We wrapped the thermistor in cling film to prevent the water conducting across the legs and altering the reading.

![](https://lh5.googleusercontent.com/cVGjJGnzkw4fELwLeoUsbL1wRIbfxg9ShtPin4vQp295qGxoxqu-XWsv05iU2n1yzrnvnpRBeRwRGEf7CMH_0qYRvcDK2pwizRB5UPe5qGjYkv-VZHLpt2PxpqGkLz1eYNpcp3vz)![](https://lh6.googleusercontent.com/DYPsAZI06tujDdSmxQke3xke5Z_tgahJoDsP99CsDfkumKsD59r77cL5TzyJ3I-dQHReJ4HWH6pJXnPTffWaae55WwsRAcyi-LeArY35kcROvp_0QCg4Sd_nd4dUlVw8wbuDazzY)![](https://lh5.googleusercontent.com/nShVV70e4TSh-BrVYO2JbfnnTc5gbaRies6huphxmKOkN3AnkHvvtmZI7KSS8se9C5wNRq2h0OMcqNMBYDlFHbNL8ViQqILDi12tUruWA_lmbL5I-AtS9YxtZoe9M_XH7DdlgQyC)

