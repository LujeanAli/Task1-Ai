# Robotic Arm Simulation in Robot Operating System (ROS)

   ![image](RobotArm.png)

## Install ROS 

1- download VirtualBox  https://www.virtualbox.org/wiki/Downloads

2- download Ubuntu 18.04  https://releases.ubuntu.com/18.04/

3- create the virtual machine 

## Install ROS melodic

1- Open terminal

2- Setup computer to accept software from packages.ros.org.
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

```

3- Set up keys

```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```

4- To make sure Debian package index is up-to-date:
```
sudo apt update
```

5- Installation

5.1- Desktop-Full Install: (Recommended) 
```
sudo apt install ros-melodic-desktop-full
```

5.2-To find available packages:
```
apt search ros-melodic
```

6- Environment setup
```
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

7- Dependencies for building packages
```
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
```

7.1- Initialize rosdep

```
sudo apt install python-rosdep
```

```
sudo rosdep init
rosdep update
```

## Creat a workspace for catkin

 Prerequisites
```
$ source /opt/ros/melodic/setup.bash
```

create and build a catkin workspace:
```
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
```

## Installing the package arduino_robot_arm

1- Add the “arduino_robot_arm” package to “src” folder

```
$ cd ~/catkin_ws/src 
```

```
$ sudo apt install git
```

```
$ git clone https://github.com/smart-methods/arduino_robot_arm
```

2- Install all the dependencies 
```
$ cd ~/catkin_ws
```
```
$ rosdep install --from-paths src --ignore-src -r -y
```
```
$ sudo apt-get install ros-melodic-moveit
```
```
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
```
```
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
```
```
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
Compile the package
```
```
$ catkin_make
```

## Controlling the motors
```
$ roslaunch robot_arm_pkg check_motors.launch
```

















