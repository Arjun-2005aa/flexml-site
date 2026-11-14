---
title: FlexML — Robot Vision for iPhone and iPad
---

# FlexML

**Your iPhone is the best vision computer your robot can have.**

FlexML runs any Core ML vision model live on the iPhone or iPad camera, anchors what it sees in 3D with ARKit and LiDAR, and streams the results to your robot, laptop or microcontroller.

- **Run any vision model:** object detection, classification, segmentation, depth, pose. Import `.mlmodel` or `.mlpackage` files, and FlexML works out the rest.
- **AR and 3D mapping:** objects stay anchored as you move; on LiDAR devices, get distances and coloured point clouds you can export as PLY.
- **Connect your robot:** JSON over WebSocket or HTTP with automatic discovery, compact UDP and Bluetooth LE output for microcontrollers, a ROS 2 bridge, and commands from the robot back to the app.
- **Private by design:** everything runs on the device. No account, no analytics, no ads.

## Get started

```
pip install flexml-companion
flexml serve
```

Open **Network Setup** in FlexML, and it finds your computer automatically.

- [Support and FAQ](support)
- [Privacy policy](privacy)
