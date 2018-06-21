# Calibrating the eChook

From the default values in the calibration.h file, the eChook board will read reasonably accurate data. This section takes you through calibrating each input in turn. Each calibration routine involves taking some readings with external equipment - generally a multimeter - some simple calculations, and updating a calibration variable in the eChook Arduino Code.

The signals that will benefit most from calibration are speed, motor RPM and temperature, followed by voltages, and then current.

