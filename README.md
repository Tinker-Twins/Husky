# Husky
### ROS Packages for Husky Robot

![](https://github.com/Tinker-Twins/Husky/blob/main/Husky.png)

## Dependencies

 - fath_pivot_mount_description: `$ sudo apt-get install ros-noetic-fath-pivot-mount-description`
 - flir_camera_description: `$ sudo apt-get install ros-noetic-flir-camera-description`
 - velodyne_description: `$ sudo apt-get install ros-noetic-velodyne-description`
 - realsense2_description: `$ sudo apt install ros-noetic-realsense2-description`
 - LMS1xx: `$ sudo apt-get install ros-noetic-lms1xx`
 - robot_localization: `$ sudo apt-get install ros-noetic-robot-localization`
 - interactive_marker_twist_server: `$ sudo apt-get install ros-noetic-interactive-marker-twist-server`
 - twist_mux: `$ sudo apt-get install ros-noetic-twist-mux`
 - teleop_twist_keyboard: `$ sudo apt-get install ros-noetic-teleop-twist-keyboard`
 - teleop_twist_joy: `$ sudo apt-get install ros-noetic-teleop-twist-joy`
 - rviz_imu_plugin: `$ sudo apt-get install ros-noetic-rviz-imu-plugin`
 - gmapping: `$ sudo apt-get install ros-noetic-gmapping`

## Installation

1. Create a Catkin workspace (if not already present)
  ```bash
  $ mkdir -p catkin_ws/src
  ```
2. Change directory to the source space (`src`) of your Catkin workspace
  ```bash
  $ cd catkin_ws/src
  ```
3. Clone this repository:
  ```bash
  $ git clone https://github.com/Tinker-Twins/Husky.git
  ```
4. Change directory back to the Catkin workspace:
  ```bash
  $ cd ..
  ```
5. Build the packages:
  ```bash
  $ catkin_make
  ```

## Usage:

1. Keyboard Teleoperation:
    ```bash
    $ roslaunch husky_gazebo husky_playpen.launch
    $ roslaunch husky_control teleop_keyboard.launch
    ```

2. Map-Less Navigation:
    ```bash
    $ roslaunch husky_gazebo husky_playpen.launch
    $ roslaunch husky_viz view_robot.launch
    $ roslaunch husky_navigation map_less_navigation.launch
    ```

3. Simultaneous Localization And Mapping (SLAM):
    ```bash
    $ roslaunch husky_gazebo husky_playpen.launch
    $ roslaunch husky_viz view_robot.launch
    $ roslaunch husky_navigation gmapping.launch
    $ roslaunch husky_control teleop_keyboard.launch
    ```
    To save generated map to current working directory, run:
    ```bash
    $ rosrun map_server map_saver -f <filename>
    ```

4. Adaptive Monte Carlo Localization (AMCL):
    ```bash
    $ roslaunch husky_gazebo husky_playpen.launch
    $ roslaunch husky_viz view_robot.launch
    $ roslaunch husky_navigation amcl.launch
    $ roslaunch husky_control teleop_keyboard.launch
    ```

5. Map-Based Navigation:
    ```bash
    $ roslaunch husky_gazebo husky_playpen.launch
    $ roslaunch husky_viz view_robot.launch
    $ roslaunch husky_navigation map_based_navigation.launch
    ```

## Video Tutorials:

1. [Installation](https://youtu.be/kXD9GfkbkHk)
2. [Teleoperation](https://youtu.be/B-4VfZrvVJo)
3. [Map-Less Navigation](https://youtu.be/3sVrWRfWrEY)
4. [SLAM](https://youtu.be/-_bC1_xs9TY)
5. [Map-Based Localization](https://youtu.be/RrX4_UMeTQ8)
6. [Map-Based Navigation](https://youtu.be/F5OiuIkqxcc)
