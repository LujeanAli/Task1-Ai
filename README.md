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











