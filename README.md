# robot_ws
This project explores an autonomous vacuum cleaner using both differential and swerve drives. We employ RP Lidar A1 for mapping and navigation, integrating SLAM (Gmapping) and the ROS navigation stack for autonomous movement and obstacle avoidance. Includes URDF models, configuration files, and launch files for ROS.

Robopeak: Autonomous Vacuum Cleaner Project
Welcome to the Robopeak project! This repository contains the code and configuration files for our autonomous vacuum cleaner. The project explores two different drive systems: differential drive and swerve drive. We also utilized an RP Lidar A1 for mapping and navigation.

Project Overview
The Robopeak project aims to develop a fully autonomous vacuum cleaner capable of navigating and cleaning various environments without human intervention. The primary goals of this project are:

To compare the performance of differential and swerve drive systems in an autonomous vacuum cleaner.
To use SLAM (Simultaneous Localization and Mapping) for accurate mapping and navigation.
To integrate sensors and control algorithms to ensure efficient cleaning.
Features
Drive Systems: We implemented both differential and swerve drive systems and compared their performance.
Mapping: Utilized RP Lidar A1 for real-time mapping and navigation.
SLAM: Integrated Gmapping for Simultaneous Localization and Mapping.
Navigation: Employed ROS navigation stack for autonomous movement and obstacle avoidance.
State Estimation: Used AMCL (Adaptive Monte Carlo Localization) for precise localization within the mapped environment.
Repository Structure
urdf/: Contains the URDF (Unified Robot Description Format) files for the robot model.
config/: Configuration files for the navigation stack, costmaps, and trajectory planner.
launch/: ROS launch files to start the robot simulation, mapping, and navigation.
maps/: Sample map files created using the RP Lidar A1.
rviz/: RViz configuration files for visualizing the robot and its environment.
scripts/: Custom scripts for various functionalities such as goal setting and sensor data processing.
world/: Gazebo world files for simulating the robot in different environments.
Getting Started
Prerequisites
ROS Noetic
Gazebo
RP Lidar A1
Other dependencies can be installed via rosdep
Installation
Clone this repository:

sh
Copy code
git clone https://github.com/yourusername/robopeak.git
cd robopeak
Install dependencies:

sh
Copy code
rosdep install --from-paths src --ignore-src -r -y
Build the workspace:

sh
Copy code
catkin_make
source devel/setup.bash
Running the Simulation
Launch the simulation environment:

sh
Copy code
roslaunch robopeak empty_world.launch
Start the SLAM process:

sh
Copy code
roslaunch robopeak gmapping.launch
Launch the navigation stack:

sh
Copy code
roslaunch robopeak move_base.launch
Visualize in RViz:

sh
Copy code
rosrun rviz rviz -d $(find robopeak)/rviz/robopeak.rviz
Contribution
We welcome contributions from the community. Please feel free to fork the repository, create a branch, and submit a pull request with your improvements. Make sure to follow the coding standards and include appropriate documentation.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Contact
If you have any questions or need further assistance, please open an issue in the repository or contact us at minaehabmegalaa@gmail.com
