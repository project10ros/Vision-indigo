Follow the steps:

Installation

Installation from prebuild packages

vision_visp stack could be installed from prebuilt packages.

	sudo apt-get install ros-indigo-vision-visp


Installation from source

vision_visp stack could also be build and installed from source code following the steps described next.

Install ROS and create a catkin workspace

    mkdir -p ~/catkin_ws/src
    cd ~/catkin_ws/src
    catkin_init_workspace
    cd ~/catkin_ws
    catkin_make

Bring the source

    cd ~/catkin_ws/src

Get vision_visp stack:

    git clone https://github.com/project10ros/Vision-indigo.git

Checkout the branch that matches your ROS distro:

    cd vision_visp
    git checkout indigo

Install dependencies

    cd ~/catkin_ws
    sudo rosdep init
    rosdep update
    rosdep install --from-paths src --ignore-src --rosdistro indigo

Build the source

    cd ~/catkin_ws
    catkin_make

Test installation

    roslaunch visp_tracker tutorial.launch
    roslaunch visp_auto_tracker tutorial.launch




After this, you have to follow the steps for usb_cam:


	mkdir -p ~/catkin-ws/src

	cd ~/catkin-ws/src

	git clone https://github.com/project10ros/Vision-indigo.git

	cd ..

	catkin_make

	source ~/catkin-ws/devel/setup.bash


