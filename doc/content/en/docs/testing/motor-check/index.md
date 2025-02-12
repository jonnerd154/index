---
title: "Motor Check"
linkTitle: "Motor Check"
weight: 20
description: >-
     How to check the motors on your Index
---

Now that you're connected to your Index, we're going to send it some Gcode and test its motors. First send it the following lines of Gcode one-by-one. These commands will set the machine to an absolute positioning system, and start the homing procedure. You should see the machine move all three linear axis and home using the three limit switches:

```
G91 ;absolute positioning
G28 ;homing procedure
```

If the X, Y, and Z axis all moved and homed correctly, excellent! If not, you might have a cable unplugged or inserted the wrong way around.

Next we'll check the left nozzle rotation stepper motor:

```
G0 A90
```

You should see your nozzle stepper rotate 90 degrees.


