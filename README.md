# ArUco marker detection and pose estimation
This lab consists of two parts:

First: the robot should follow the outside block loop starting from the position marked "start" .

Second: During the process of line following, the robot should look for an ArUco marker with the ID = 14, which is placed at the end of the two parallel lines, before coming to a stop in front of the marker.

## Step 1. clone the source code
git clone git@github.com:g0531/ArUco-marker-detection-and-pose-estimation.git
## Step 2. catkin make all the download package
cd ~/catkin_ws

catkin_make
## Step 3. run roscore
roscore
## Step 4. SBC(raspberrypi) set up
roslaunch turtlebot3_bringup turtlebot3_robot.launch

roslaunch raspicam_node camerav2_410x308_30fps.launch

## Step 5. roslaunch on PC to find the ArUco marker
roslaunch aruco_marker_finder.launch markerID:=14 markerSize:=0.05
## Step 6. roslaunch detect and navigate on PC
roslaunch line_follower_turtlebot lf.launch

