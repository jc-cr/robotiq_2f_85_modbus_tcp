# Robotiq 2F 85 Gripper ROS Package

This package provides a simple ROS interface for the Robotiq 2F 85 gripper using the Modbus TCP protocol. 

Code is based on the following: 
- https://gist.github.com/felixvd/d538cad3150e9cac28dae0a3132701cf
- https://sdurobotics.gitlab.io/ur_rtde/guides/guides.html#use-with-robotiq-gripper

## Usage

This package exposes the following ROS services:

- `/robotiq_2f_85_gripper_control/open`: Opens the gripper
- `/robotiq_2f_85_gripper_control/close`: Closes the gripper
- `/robotiq_2f_85_gripper_control/set_goal_position`: Sets the gripper to a specific position
- `/robotiq_2f_85_gripper_control/auto_calibrate`: Performs auto-calibration of the gripper

And the following ROS topics:

- `/robotiq_2f_85_gripper_control/current_position`: Publishes the current normalized position of the gripper (0.0 to 1.0)
- `/robotiq_2f_85_gripper_control/status`: Publishes the current status of the gripper (1.0 for active, 0.0 for inactive)
