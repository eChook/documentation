# Building the eChook Board

This section covers how to build the eChook nano board if you have bought a kit from Greenpower.

## Board Version differences

v1.3 is the first production version as sold by Greenpower, earlier versions are prototypes. This guide is aimed at V1.3 but should apply to all boards unless stated below.

### V1.0

Any V1.0 board will already be assembled and partially tested so the ‘build stage’ is not required - you can skip this bit!

The connection outputs and component references changed after V1.0, so it is not

NOTE: for V1.0 it is important that before power is applied to the board the DCDC converter is set to the right voltage with the Arduino, Bluetooth module and op-amp unplugged. Later boards do not have adjustable power supplies so this instruction no longer applies.

### V1.1, V1.2

These revisions had the following changes:

* Changed to a fixed 5V DC-DC regulator.
* Increased solder pad sizing.
* Moved all components to the same side of the PCB.
* Altered Board layout.
* Added labelled multimeter test points to the bottom of the board.
* Moved the BT module off-board
* Improved Silkscreen.
* Increased tolerances to avoid manufacturing errors.
* Added logo and component values to silkscreen.
* Changed to a white board \(solder mask\) with black silkscreen.

The initial batch of V1.2 boards had some manufacturing errors, resulting in it being easy to bridge a pad to the ground plane when soldering the board. This drove the change in tolerances, increasing the overlap of the solder mask over the ground plane around component pads. The issue is detailed [here](http://wechook.com/?p=778).

V1.2 was the first board sold in kit form - the V1.3 build instructions apply to V1.2 as well.

### V1.3

The first version of the board sold in kit form through Greenpower for the 2018 season.

Changelog:

* Added current sensor multimeter test point.
* Changed silkscreen to reflect new echook.uk website.

