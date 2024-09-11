# Installing ROS Noetic on Ubuntu 20.04

You can follow the official installation instructions from the ROS Wiki [here](http://wiki.ros.org/noetic/Installation/Ubuntu).
Below are the steps to install ROS Noetic on Ubuntu:

### 1-Add the ROS repository to your system's sources list:
```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'```

### 2-Install curl if not already installed:
```sudo apt install -y curl```

### 3-Download and add the ROS GPG key:
```curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -```

### 4-Update your package list:
```sudo apt update -y```

### 5-Install ROS Noetic (desktop full version):
```sudo apt install ros-noetic-desktop-full```

### 6-Add the ROS environment setup to your bash configuration file:
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

### 7-Install essential ROS dependencies:
```sudo apt install -y python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential```

### 8-Initialize rosdep (this is required for dependency management):
```
sudo apt install -y python3-rosdep
sudo rosdep init
rosdep update
