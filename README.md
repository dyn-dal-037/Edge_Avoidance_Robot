# Edge Avoiding Robot (ROS 2 Humble)

A ROS 2 Humble simulation project of a differential-drive robot that detects table edges / cliff-like drops and avoids driving off them using a forward-facing (tilted) LiDAR concept in Gazebo, visualized in RViz.  
This workspace is organized into separate packages for description, control, bringup, and the Python behavior node.  
Project inspiration/tutorial: https://github.com/MechaMind-Labs/Edge_Avoiding_Robot (original reference).  

---

## Tested on
- Ubuntu 22.04
- ROS 2 Humble

---

## Workspace structure

- `bot_description/`
  - URDF/Xacro robot model, Gazebo world(s), RViz config, and launch files.
- `bot_controller/`
  - ros2_control controller configs + controller launch.
- `bot_bringup/`
  - Main bringup launch that starts the full simulation stack.
- `bot_script/`
  - Python node implementing edge detection / avoidance logic.

---

## Dependencies

Install ROS 2 Humble (desktop) and common build tools, then:

```bash
sudo apt update
sudo apt install -y python3-colcon-common-extensions python3-rosdep git
sudo rosdep init || true
rosdep update
