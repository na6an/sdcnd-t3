# System Integration
### Programming a Real Self-Driving Car


## Run
`cd ~(path-to)/CarND-Capstone/ros`  
Then,  
```
cd ros  
catkin_make  
source devel/setup.sh  
roslaunch launch/styx.launch  
```


## Code Structure

  <img src="https://github.com/na6an/sdcnd-t3/blob/master/P3_System_Integration/img/final-project-ros-graph-v2.png" alt="alt text" width="920" height="640">  

Below is a brief overview of the repo structure, along with descriptions of the ROS nodes.  
The code that you will need to modify for the project will be contained entirely within the  
/ros/src/ directory. Within this directory, you will find the following ROS packages:

/ros/src/tl_detector/  
This package contains the traffic light detection node: tl_detector.py.  
This node takes in data from the /image_color, /current_pose, and /base_waypoints topics  
and publishes the locations to stop for red traffic lights to the /traffic_waypoint topic.

The /current_pose topic provides the vehicle's current position,  
and /base_waypoints provides a complete list of waypoints the car will be following.

You will build both a traffic light detection node and a traffic light classification node.  
Traffic light detection should take place within tl_detector.py,  
whereas traffic light classification should take place within ../tl_detector/light_classification_model/tl_classfier.py.


/ros/src/waypoint_updater/
This package contains the waypoint updater node: waypoint_updater.py.  
The purpose of this node is to update the target velocity property of each waypoint  
based on traffic light and obstacle detection data.  
This node will subscribe to the /base_waypoints, /current_pose, /obstacle_waypoint,  
and /traffic_waypoint topics, and publish a list of waypoints ahead of the car  
with target velocities to the /final_waypoints topic.


/ros/src/twist_controller/
Carla is equipped with a drive-by-wire (dbw) system, meaning the throttle, brake, and steering have electronic control.  
This package contains the files that are responsible for control of the vehicle: the node dbw_node.py and the file twist_controller.py, along with a pid and lowpass filter that you can use in your implementation. The dbw_node subscribes to the /current_velocity topic along with the /twist_cmd topic to receive target linear and angular velocities. Additionally, this node will subscribe to /vehicle/dbw_enabled, which indicates if the car is under dbw or driver control. This node will publish throttle, brake, and steering commands to the /vehicle/throttle_cmd, /vehicle/brake_cmd, and /vehicle/steering_cmd topics.
