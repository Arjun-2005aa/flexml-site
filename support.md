---
title: FlexML Support
---

# FlexML Support

Need help? Email **[arjun.kondala2005@gmail.com](mailto:arjun.kondala2005@gmail.com)**. Please include your device model, iOS version, FlexML version (Settings › About) and, for model problems, what `flexml check-model` says about your model.

## Getting started

1. Open FlexML. A sample detection model is already selected.
2. Tap **Start Inference** and point the camera at everyday objects.
3. To connect a computer or robot, install the free companion on a computer on the same Wi-Fi:
   ```
   pip install "flexml-companion[all] @ git+https://github.com/Arjun-2005aa/FlexML_SDK.git#subdirectory=python"
   flexml serve
   ```
   FlexML finds it automatically under **Network Setup**.

Full guides, examples and the data reference are in the **[FlexML SDK](https://github.com/Arjun-2005aa/FlexML_SDK)**: [Getting started](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/getting-started.md) · [Bring your own model](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/bring-your-own-model.md) · [Robot integration](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/robot-integration.md) · [Data reference](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/data-reference.md) · [ESP32 examples](https://github.com/Arjun-2005aa/FlexML_SDK/tree/main/examples/esp32) · [ROS 2](https://github.com/Arjun-2005aa/FlexML_SDK/tree/main/examples/ros2)


## FAQ

**Which models work?**
Core ML models (`.mlmodel`, `.mlpackage`) with an image input: object detection, classification, segmentation, depth, pose and image-to-image. Models from Create ML and Ultralytics YOLO exports work directly, and others can be converted with Apple's [coremltools](https://github.com/apple/coremltools). Tap ⓘ next to a model to see what FlexML detected.

**My model shows "This model takes numbers, not an image".**
Re-export it with an image input (`ct.ImageType` in coremltools). The [model guide](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/bring-your-own-model.md) explains how.

**The boxes are in the wrong place.**
Open **Display › Fit frame to model** and try **Fit** for YOLO models or **Center crop** for classifiers.

**AR, distances or point clouds aren't available.**
AR needs a device that supports ARKit world tracking. Distances and point clouds need a LiDAR sensor (Pro iPhone models from iPhone 12 Pro, and iPad Pro). FlexML shows which features your device supports on the home screen.

**FlexML can't find my computer.**
Make sure the phone and computer are on the same Wi-Fi network, that `flexml serve` is running, and that FlexML has Local Network permission (Settings › Privacy & Security › Local Network). You can also type the computer's IP address under **Network Setup**, or scan the QR code that `flexml serve` prints (included when you install with `[all]` as above).

**Does FlexML send my camera or data anywhere?**
No. Everything runs on your device, and data goes only to a computer or robot that you connect. See the [privacy policy](privacy).

**How do I get the 3D point cloud on my computer?**
Switch to **AR** mode with `flexml serve --map room.ply` running; the point cloud streams about once a second and is saved when you press Ctrl-C. It's sent over Wi-Fi to a computer only (not to microcontrollers over UDP or Bluetooth). LiDAR devices give a dense coloured cloud; others give sparse points. Details in the [data reference](https://github.com/Arjun-2005aa/FlexML_SDK/blob/main/docs/data-reference.md#the-point-cloud-in-detail).

**How do I get my recordings and maps off the phone?**
Use **Recordings** or **Spaces** on the home screen and tap Share. Point clouds export as PLY files that open in MeshLab, CloudCompare, Open3D and Blender.
