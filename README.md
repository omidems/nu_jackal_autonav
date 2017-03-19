Winter Quarter Project: Autonomous Navigation
==============
### Using a Clearpath Jackal UGV and the ROS Navigation Stack

#### *Nate Kaiser - Northwestern MS in Robotics Winter Quarter Project*

![][1]

## Overview
This package, along with its dependencies, provide everything necessary to navigate the Northwestern Robotics Program's [Clearpath Jackal UGV][2] autonomously using laser data from a [Velodyne VLP-16 LIDAR][3].

Specifically, this package uses:
- Either the default [global_planner][4] or [NavFN][5] for global path planning
- Either gmapping or hector_slam for SLAM/mapping
- AMCL for localizing within a given map
- A custom local planner is in the works but is not yet fully implemented

Parameters have been tuned specifically for Northwestern's robot/environment combination, so some tweaks may be necessary if this is ported to a different robot or environment.


## Installation
#### Prerequisites
To install, fire up a terminal and run:

`sudo apt-get install ros-indigo-velodyne ros-indigo-velodyne-description ros-indigo-velodyne-simulator ros-indigo-jackal-desktop ros-indigo-jackal-gazebo`

Alternatively, I hope to add `rosdep install name-of-package` functionality in the near future.

This will need to be done on both the host computer and Jackal's computer, but Jackal should already have `ros-indigo-jackal-desktop` installed, and has no need for `ros-indigo-jackal-gazebo`, since Gazebo simulations will only be run on the host computer.

Note: this assumes you already have a ***full*** ROS Indigo installation (`ros-indigo-desktop-full`) running on Ubuntu 14.04. If not, you may have to install other dependencies that come with the full version (PCL, OpenCV, etc). Also, this package *should* work on a different ROS version or Linux version/distro, but no testing has been done to verify.

#### This Package


HOW DO THEY GET/INSTALL IT on comp/then on Jackal?
- download my package and build
  - I recommend catkin build tools (link to apt-get command)
- install and set up communication w/ Jackal

-ubuntu 14.04, ros indigo (full install includes PCL/OpenCV)
rosdep install _
or sudo apt-get _


## Instructions For Use

HOW DO THEY USE IT?


## Specifics
- xyz location of the laser
- configs set for floor type (slick for wheels)
- proximity to stuff when navigating = close, also highly dynamic
- most modifiable parameters stored in config files or launch files


## Future Work
- currently working on custom local planner, will release as separate package when finished


## Other Considerations?
- fast, empty router necessary?


<!-- File Locations -->
[1]: https://github.com/njkaiser/Winter_Project/blob/master/media/navigating_laser_only.gif
[2]: https://www.clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/
[3]: http://velodynelidar.com/vlp-16.html
[4]: http://wiki.ros.org/global_planner?distro=indigo
[5]: http://wiki.ros.org/navfn?distro=indigo
[6]:
[7]:
[8]:
[9]:
[10]:
