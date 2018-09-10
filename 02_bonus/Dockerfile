FROM osrf/ros:kinetic-desktop-xenial

RUN echo "Now updating packages and system to latest version."

RUN apt-get update && apt-get install -y --no-install-recommends apt-utils && apt-get upgrade -y && apt autoremove -y

RUN echo "\n Installing git, pip, xclip and vim"

RUN apt-get install git python-pip vim xclip -y

RUN echo " Install ros"

RUN apt-get install ros-kinetic-desktop-full -y

RUN apt-get install -y python-rosinstall python-rosinstall-generator python-wstool build-essential

RUN apt-get install -y javascript-common libjs-jquery libjs-sphinxdoc libjs-underscore python-catkin-lint python-catkin-lint python-catkin-tools python-concurrent.futures  python-osrf-pycommon  python-rosdep  python-trollius python-wstool python-pandas ros-kinetic-gazebo-ros-control  ros-kinetic-gazebo-ros-control   ros-kinetic-gazebo-ros-pkgs ros-kinetic-gazebo-ros-pkgs ros-kinetic-geometry-msgs  ros-kinetic-joy  ros-kinetic-ros-control ros-kinetic-ros-controllers ros-kinetic-rosserial ros-kinetic-rosserial-arduino ros-kinetic-serial ros-kinetic-teleop-tools ros-kinetic-teleop-twist-joy ros-kinetic-xacro ros-kinetic-web-video-server ros-kinetic-teb-local-planner     ros-kinetic-hector-slam ros-kinetic-map-server ros-kinetic-amcl ros-kinetic-tf2-sensor-msgs ninja-build ros-kinetic-sick-tim ros-kinetic-rplidar-ros

RUN mkdir -p /home/root/catkin_ws

WORKDIR /home/root/catkin_ws

# Work dockerfile so obscured the login details
RUN git clone https://xxxxx:xxxxxxxxxxxxxxxxxxxxxxxx@github.com/xxxx/xxxx.git

RUN wstool init src

RUN wstool merge -t src manifest/ros_install/maryam-release3.rosinstall

RUN apt-get install ssh-client -y

RUN ls /home/root/catkin_ws

RUN wstool update -t src
