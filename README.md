# Posenet++
1. It solves the **Kidnapped-Robot problem** by regressing poses of images that are part of a scene(used KITTI dataset's left image and poses ground truth).
2. [Paper Link](https://posenet-mobile-robot.github.io/etc/Team%2016%20-%20ROB%20530.pdf)
## Implementation of PoseNet++
* It reuses VGG16 model coupled with Dense layers(4096, 4096) with a linear activation function(Wx+B) on the output, to regress poses of the input image scene.
* It has a custom loss function for rotation and translation componenets.
* **sqrt(L2_norm(y_pred, y_actual)** for loss is used for both translation and rotation, with a _Beta_ penalty factory for rotation only.

## TODOs:
* Implement GTSAM and use this CNN based pose-regressor as a sensor along with other sensors such as GPS, IMU, etc for reliable odometry source.
