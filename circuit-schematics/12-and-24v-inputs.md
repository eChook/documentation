## **24v and 12v interface**

![](https://lh4.googleusercontent.com/3dqEng96hjpyZ2TGc14n3yMBvOySjo-OmNm2KM1m6NvkkP55jNfYTt651rU0modOr0cWeWOQhuywFpl-0hR0gtRoK-O_QZEt2r7qXEDnJOVWC9U_HNJWF7WJr8MN1OHGIE6hJPDr)

Each of the battery voltages need to be stepped down so that in worst case the voltage seen at the arduino won’t exceed 5v. To achieve this a potential divider was chosen to step 30v down to 5v. Each voltage input uses the same component values.

Resistors R1 and R2 above form the potential divider.

C3 is a ceramic capacitor forming a low pass filter with R1 and R2 to remove any high frequency component from the voltage signal. On a greenpower car the motor will produce small high frequency voltage spikes as the brushes connect and disconnect from the commutator, the low pass filter removes these from the signal reaching the arduino.

BattTotalVTP represents the multimeter test point on the back of the PCB, giving easy access to check the voltage output from the potential divider with a multimeter or oscilloscope.

The circuit to the right is identical, but takes the lower battery voltage as an input.

  


