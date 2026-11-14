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
   pip install flexml-companion
   flexml serve
   ```
   FlexML finds it automatically under **Network Setup**.


## FAQ

**Which models work?**
Core ML models (`.mlmodel`, `.mlpackage`) with an image input: object detection, classification, segmentation, depth, pose and image-to-image. Models from Create ML and Ultralytics YOLO exports work directly, and others can be converted with Apple's coremltools. Tap ⓘ next to a model to see what FlexML detected.

**My model shows "This model takes numbers, not an image".**
Re-export it with an image input (`ct.ImageType` in coremltools). The model guide explains how.

**The boxes are in the wrong place.**
Open **Display › Fit frame to model** and try **Fit** for YOLO models or **Center crop** for classifiers.

**AR, distances or point clouds aren't available.**
AR needs a device that supports ARKit world tracking. Distances and point clouds need a LiDAR sensor (Pro iPhone models from iPhone 12 Pro, and iPad Pro). FlexML shows which features your device supports on the home screen.

**FlexML can't find my computer.**
Make sure the phone and computer are on the same Wi-Fi network, that `flexml serve` is running, and that FlexML has Local Network permission (Settings › Privacy & Security › Local Network). You can also type the computer's IP address under **Network Setup**, or scan the QR code that `flexml serve` prints (install `flexml-companion[qr]` to get it).

**Does FlexML send my camera or data anywhere?**
No. Everything runs on your device, and data goes only to a computer or robot that you connect. See the [privacy policy](privacy).

**How do I get my recordings and maps off the phone?**
Use **Recordings** or **Spaces** on the home screen and tap Share. Point clouds export as PLY files that open in MeshLab, CloudCompare, Open3D and Blender.
