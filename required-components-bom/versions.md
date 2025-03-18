---
description: There are separate Kit versions and Board(PCB) versions
---

# Versions

## Kit Versions

### V1.3

First version of the kit sold by Greenpower with PCB v1.3

### V1.4

Introduced in 2022, minor changes to the kit, now includes a second PCB for mounting the current sensor. Still uses PCB v1.3.

### V1.5

Introduced in 2023, minor changes to the kit, replacing the Arduino Nano 328P Clone with a Genuine Arduino Nano Every development board.

### V2.0

Introduced in 2025, and including some major changes. The kit includes the new V2.0, pre-assembled eChook board. Also includes a new magnet sensor board to make mounting and testing the Wheel and Motor RPM Sensors easier.

## PCB Version differences

v1.3 is the first production version as sold by Greenpower, earlier versions are prototypes. This guide is aimed at V1.3 but should apply to all boards unless stated below.

### V1.0

Any V1.0 board will already be assembled and partially tested so the ‘build stage’ is not required - you can skip this bit!

The connection outputs and component references changed after V1.0, so the pin out's aren't all compatible!

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
* Changed to a white board (solder mask) with black silkscreen.

The initial batch of V1.2 boards had some manufacturing errors, resulting in it being easy to bridge a pad to the ground plane when soldering the board. This drove the change in tolerances, increasing the overlap of the solder mask over the ground plane around component pads. The issue is detailed [here](http://wechook.com/?p=778).

V1.2 was the first board sold in kit form - the V1.3 build instructions apply to V1.2 as well.

### V1.3

The first version of the board sold in kit form through Greenpower for the 2018 season.

Changelog:

* Added current sensor multimeter test point.
* Changed silkscreen to reflect new echook.uk website.

### V1.3.1

The eChook team has moved from using DesignSpark PCB to KiCad for schematic capture and PCB design. It wasn't possible to import V1.3 into KiCad so it was recreated.&#x20;

* Component placement virtually unchanged.
* Tracks Rerouted.
* Test Point placement improved.
* Silkscreen Improved.

This version is used for any 3D renders in this document and the Virtual iBom build aid - both features enabled by the move to KiCad. There are no current plans to fabricate v1.3.1.

### V2.0

Version 2.0 of the board contains some major changes, but retains the same features. It is the same size as earlier versions, has the same connections, and uses the same code.

It moves away from an assemble yourself kit, to a pre-assembled board with predominantly surface mount components - this has enabled a higher component count, more complex circuits offering a far more electronically robust board. There is a blog post going into more details of the changes [here](https://shop.echook.uk/?p=444).

