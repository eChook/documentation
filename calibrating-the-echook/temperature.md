# Temperature

These are the most involved sensors to calibrate, primarily due to the response of the thermistors being non-linear. A typical 10kΩ thermistor resistance vs temperature graph is shown below:

![](https://lh4.googleusercontent.com/z8hZ8SvbFAUlVafoLBIffR0ba-W5_rT01rHz17n3Jz-88D0F088MpPB4ndDL4eUz13awJpIQm42ru8HbgTlM9KoGhY0lbiR4WjP_GLsFwfe0UgLFJYWsLyTQnudFe_yAKh3eBetC)

Note that the 10k refers to the resistance at room temperature \(25°\), and that the resistance decreases as temperature increases. This is called a negative temperature coefficient, or NTC. The eChook board uses a 10k NTC Thermistor.

On the board, the thermistor completes the lower half of a potential divider circuit with a 10kΩ resistor, as such the voltage at the output of the potentiometer falls as the temperature of the thermistor increases.

To translate this voltage to a temperature, the resistance curve of the specific thermistor being used is needed. Due to tolerances, this is subtly different even between identical thermistors. To do this the eChook uses the [Steinhart–Hart](https://en.wikipedia.org/wiki/Steinhart–Hart_equation) equation which uses three coefficients calculated from the thermistor to convert the resistance seen to an accurate temperature reading.

The first step in calibrating the thermistor is calculating these coefficients. Thankfully there’s a useful online calculator to help! All that is required is three measurements of the resistance of the thermistor at different, known temperatures. The calculator can be found [here](https://www.thinksrs.com/downloads/programs/therm%20calc/ntccalibrator/ntccalculator.html) and looks like this:

![](https://lh3.googleusercontent.com/fmYhUC_dDDkDMKbMWPzaOq1qHJJ6kehtJjfd_UuTrWpTaNHCxvm0np7ymCy6kjwasyXHZBpfv9XZsvGpLbHzfyuvvEAgYeeR0o73np7Ed0G2BduqZFHUd_0shGBJHHU87K6xzmo4)

Enter the three temperature and resistance measurements and copy the A, B and C coefficients from the calculator into the calibration.h file.

```text
//Board and Sensor Specific Calibrations
const float CAL_THERM_A = 0.001871300068; //Steinhart-Hart constants - See documentation for calibration method
const float CAL_THERM_B = 0.00009436080271;
const float CAL_THERM_C = 0.0000007954800125;
```

To get the default calibration we used a pan of water, digital thermometer and a multimeter. We wrapped the thermistor in cling film to prevent the water conducting across the legs and altering the reading.

![](https://lh5.googleusercontent.com/cVGjJGnzkw4fELwLeoUsbL1wRIbfxg9ShtPin4vQp295qGxoxqu-XWsv05iU2n1yzrnvnpRBeRwRGEf7CMH_0qYRvcDK2pwizRB5UPe5qGjYkv-VZHLpt2PxpqGkLz1eYNpcp3vz)![](https://lh6.googleusercontent.com/DYPsAZI06tujDdSmxQke3xke5Z_tgahJoDsP99CsDfkumKsD59r77cL5TzyJ3I-dQHReJ4HWH6pJXnPTffWaae55WwsRAcyi-LeArY35kcROvp_0QCg4Sd_nd4dUlVw8wbuDazzY)![](https://lh5.googleusercontent.com/nShVV70e4TSh-BrVYO2JbfnnTc5gbaRies6huphxmKOkN3AnkHvvtmZI7KSS8se9C5wNRq2h0OMcqNMBYDlFHbNL8ViQqILDi12tUruWA_lmbL5I-AtS9YxtZoe9M_XH7DdlgQyC)

