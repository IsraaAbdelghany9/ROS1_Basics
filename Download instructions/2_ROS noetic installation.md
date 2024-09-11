# Installing ROS Noetic on Ubuntu 20.04

ROS Noetic is the latest long-term support (LTS) version of ROS and will receive updates until **May 2025**. 
Ubuntu is preferred by many ROS users because it has a large user base, which means there is extensive community support.
If you run into any issues with ROS packages, you can consult the following resources:

- **[ROS Wiki](http://wiki.ros.org/)**: Detailed documentation for ROS.
- **[ROS Answers](https://answers.ros.org/)**: A Q&A forum for troubleshooting and community support.

### ROS Noetic Installation on Ubuntu 20.04

You can follow the official installation instructions from the ROS Wiki [here](http://wiki.ros.org/noetic/Installation/Ubuntu).

Below are the steps to install ROS Noetic on Ubuntu:

## Add the ROS repository to your system's sources list:
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

## Install curl if not already installed:
sudo apt install -y curl

## Download and add the ROS GPG key:
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

## Update your package list:
sudo apt update -y

## Install ROS Noetic (desktop full version):
sudo apt install ros-noetic-desktop-full

## Add the ROS environment setup to your bash configuration file:
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

## Install essential ROS dependencies:
sudo apt install -y python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

## Initialize rosdep (this is required for dependency management):
sudo apt install -y python3-rosdep
sudo rosdep init
rosdep update
