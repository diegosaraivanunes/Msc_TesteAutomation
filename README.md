# Msc_TestAutomation

# ROS Setup 
- Install- http://wiki.ros.org/melodic/Installation/Ubuntu \n
- Configure ROS Environment - http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment

# Moveit install
- https://moveit.ros.org/install/
- https://ros-planning.github.io/moveit_tutorials/doc/getting_started/getting_started.html

# Fanuc drivers
- http://wiki.ros.org/fanuc_driver?distro=melodic

- Important note - Melodic Compability:

# Fanuc dirvers to LRMate200id 
- https://github.com/ros-industrial/fanuc_experimental.git

# Camera
## Intrinsic Calibration
The calibration was done following this [tutorial](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration).

Node publishing images over ROS:
```
rosrun usb_cam usb_cam_node 
```
To start the calibration you will need to load the image topics that will be calibrated: 
```
rosrun camera_calibration cameracalibrator.py --size 9x7 --square 0.025 image:=/usb_cam/image_raw camera:=/usb_cam  --no-service-check
```
Interface

Results

## Extrinsic Calibration 
