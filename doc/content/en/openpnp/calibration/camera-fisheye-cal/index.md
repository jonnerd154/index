---
title: "Camera Fisheye Calibration"
linkTitle: "Camera Fisheye Calibration"
weight: 10
type: docs
description: >
  Applying fisheye calibration to the cameras
---

Awesome! Now we've got OpenPnP installed on your computer, and we've got the default Index configuration loaded up, our next step is calibrating the fisheye out of the camera lenses. Almost all of the settings in this menu are preset for the machine, but there are a few that you'll need to do for your specific machine. Lens Fisheye Calibration is one of these.

1. Click on the `Machine Setup` tab along the top of the UI

{{< container-image path="images/Screen Shot 2022-01-11 at 12.34.46 PM.png" alt="" >}}

2. What you see is a tree of all the components of a Pick and Place machine. We recommend expanding this menu using the `Expand` check box to see the full depths of the objects.

{{< container-image path="images/Screen Shot 2022-01-11 at 12.38.43 PM.png" alt="" >}}

3. Now, look under the `Cameras` menu (not the one under Reference Head H1, but instead the one with no parent elements), and click on `OpenPnpCaptureCamera Bot`. You should see a menu appear underneath. This is how settings are edited in OpenPnP: an element is clicked in this tree view, and you can change its settings in the menu below.

{{< container-image path="images/Screen Shot 2022-01-11 at 12.36.26 PM.png" alt="" >}}

4. Next, we need to make sure OpenPnP can see the cameras. Click on the `Device Settings` tab in the camera settings menu, and for the "Device" dropdown select "PnP Camera Bottom???". Make sure the format is set to ?????.

4.  In the camera settings menu, click the `Lens Calibration` tab, then click "Start Lens Calibration".

5. OpenPnP is now looking for a very specific pattern of dots which it uses to figure out how fisheyed the view is, and correct it. Hold your datum board over the bottom camera and using the viewfinder, move the calibration pattern around the camera's field of view until OpenPnP tells you that it's gathered enough photos. Make sure it's in focus of the camera, otherwise it'll have a hard time finding the pattern. If the focal distance is too close such that you can't get the whole pattern in focus and in the field of view, screw in the lens a few turns and test again.

{{< alert color="info" title="Tip" >}}
To see both camera views at the same time, click on the dropdown in the top left of the UI and select "Show All Horizontal".
{{< /alert >}}

6. Now, we'll do the top camera. Go through the same process of configuring the camera in OpenPnP, but instead of finding the top camera in the "Camera" menu, you'll find it under `Heads -> Reference Head H1 -> Cameras`.

{{< container-image path="images/Screen Shot 2022-01-11 at 12.40.48 PM.png" alt="" >}}

{{< alert color="warning" title="Heads Up" >}}
Some computers' USB hub controller has a hard time processing two video feeds through the same USB port. If your computer has a fast enough chip, you'll be able to see both feeds at the same time and connect to the motherboard using just the one USB-C cable. If not, you might need to unplug one or both of your webcam's USB cables from the motherboard, and into two different USB ports on your computer (preferably with different USB hub chips driving them).
{{< /alert >}}