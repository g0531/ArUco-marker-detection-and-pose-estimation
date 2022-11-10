# ArUco marker detection and pose estimation
This is the lab4 resources for SUSTech EE346.
## Usage
### 1.Clone the source code
cd ~/catkin_ws/src
git clone git@github.com:g0531/ArUco marker detection and pose estimation.git
### 2.Catkin make all the download package
cd ~/catkin_ws

catkin_make
### 3.Run roscore
roscore
### 4.launch bringup and camera on the SBC(Raspberry Pi)
roslaunch turtlebot3_bringup turtlebot3_robot.launch

roslaunch raspicam_node camerav2_410x308_30fps.launch
### 5.launch aruco_marker_finder on the PC
roslaunch aruco_marker_finder.launch markerID:=14 markerSize:=0.05
### 6.launch detect and navigate on the PC
roslaunch line_follower_turtlebot lf.launch
