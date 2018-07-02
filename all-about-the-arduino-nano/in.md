# The eChook nano Code

The Arduino code for the eChook nano has been written with the aim of being as easy to understand as possible with clear comments throughout, however due to the number of things the arduino needs to do, there is a lot of code to sort through. This section aims to break each area of code down into manageable chunks.

N.B. Due to the nature of the project the code may have been updated, and the extracts in this document may not perfectly match.

The code for the eChook nano is available [here](https://github.com/eChook/eChook-Arduino-Nano).

## Constants

A large section of the code is dedicated to defining constants. The first batch are pin assignments. These give a function related name for each pin, otherwise it would be necessary to remember which pin number is connected to which input and output.

The second batch of constant definitions are values used in timings and calculations.

## Setup

The setup function contains the first code run on the arduino after power on. As such it contains all the one-off setup procedures.

