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
pip install "flexml-companion[all] @ git+https://github.com/Arjun-2005aa/FlexML_SDK.git#subdirectory=python"
flexml serve
```

Open **Network Setup** in FlexML, and it finds your computer automatically.

## For developers

The free, open-source **[FlexML SDK](https://github.com/Arjun-2005aa/FlexML_SDK)** has everything for the receiving side: the Python library, a ROS 2 bridge, ESP32 examples (Wi-Fi and Bluetooth), the full data reference and an `AGENTS.md` so your AI coding agent understands it.

- [Getting started](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/getting-started.md)
- [What data you can get](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/data-reference.md) (detections, 3D pose, object map, point cloud)
- [Robot integration](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/robot-integration.md) (commands, ESP32, ROS 2)
- [Bring your own model](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/bring-your-own-model.md) (convert with Apple's [coremltools](https://github.com/apple/coremltools))
- [Project ideas](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/use-cases.md)

- [Support and FAQ](support)
- [Privacy policy](privacy)
