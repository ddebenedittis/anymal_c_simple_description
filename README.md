# ANYmal C Robot Description (URDF)
## Changes
- The package is for ROS 2 now: updated the launch file and the rviz config file, changed the command to find the meshes in the .xacro, and changed the `package.xml` and `CMakeLists.txt` files.
- Added a .xacro file for gazebo simulation purposes (`anymal_gazebo.xacro`). This file adds the ros2_control plugin, an imu sensor and the joint torques controller.

## Overview

This package contains a simplified robot description (URDF) of the [ANYmal C robot](https://www.anybotics.com/anymal) developed by [ANYbotics](https://www.anybotics.com).

The extended ANYmal C robot description, simulation, and control software is available exclusively to members of the [ANYmal Research community](https://www.anymal-research.org). For more information and membership applications, contact info@anybotics.com.

**Author & Maintainer: Linus Isler, [ANYbotics](https://www.anybotics.com)**

![ANYmal C Robot Description](doc/anymal_c_rviz.png)

## License

This software is released under a [BSD 3-Clause license](LICENSE).


## Usage

To visualize and debug the robot description, start the standalone visualization (note that you have to provide the following additional dependencies: `joint_state_publisher`, `joint_state_publisher_gui`, `robot_state_publisher`, `rviz2`, `xacro`):

    ros2 launch anymal_c_simple_description standalone.launch.py

### Launch files

* **`standalone.launch`:** A standalone launch file that starts RViz and a joint state publisher gui to debug the description.
