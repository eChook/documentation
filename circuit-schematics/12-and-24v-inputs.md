# 12 and 24V Inputs

![](https://lh4.googleusercontent.com/3dqEng96hjpyZ2TGc14n3yMBvOySjo-OmNm2KM1m6NvkkP55jNfYTt651rU0modOr0cWeWOQhuywFpl-0hR0gtRoK-O_QZEt2r7qXEDnJOVWC9U_HNJWF7WJr8MN1OHGIE6hJPDr)

Each battery voltage needs to be stepped down so that, in the worst case, the voltage seen at the Arduino does not exceed 5V. To achieve this, a potential divider was chosen to step 30V down to 5V. Each voltage input uses the same component values.

Resistors R1 and R2 above form the potential divider.

C3 is a ceramic capacitor that forms a low-pass filter with R1 and R2 to remove high-frequency components from the voltage signal. On a Greenpower car, the motor produces small high-frequency voltage spikes as the brushes connect and disconnect from the commutator. The low-pass filter removes these from the signal reaching the Arduino.

BattTotalVTP represents the multimeter test point on the back of the PCB, giving easy access to check the voltage output from the potential divider with a multimeter or oscilloscope.

The circuit to the right is identical, but takes the lower battery voltage as an input.

