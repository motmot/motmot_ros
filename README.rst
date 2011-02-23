**********
motmot_ros
**********

motmot_ros let you use the `motmot camera utility suite
<http://code.astraw.com/projects/motmot/>`_ within `Robot Operating
System (ROS) <http://www.ros.org>`_. Specifically, it is a ROS stack
incorporating several ROS packages:

 * `camiface_ros <http://github.com/motmot/camiface_ros/>`_ - Capture image
   streams using libcamiface for the Robot Operating System (ROS)

Installation
************

(These instructions are modeled after the `ROS kinect package
<http://www.ros.org/wiki/kinect>`_.) These instructions were tested on
Ubuntu Lucid (10.04).

 0. `Install motmot <http://code.astraw.com/projects/motmot/download.html#id4>`_.

 1. `Install ros-cturtle-base <http://www.ros.org/wiki/cturtle/Installation/Ubuntu>`_.
    (This stack depends on other required stacks, such as image_pipeline.)

 2. Get the rosinstall tool::

      sudo apt-get install python-stdeb
      pypi-install rosinstall

 3. wget the motmot_ros.rosinstall file from github::

      wget http://github.com/motmot/motmot_ros/raw/master/motmot_ros.rosinstall --no-check-certificate

 4. Download motmot_ros into ``~/motmot-ros-devel``::

      rosinstall ~/motmot-ros-devel /opt/ros/cturtle motmot_ros.rosinstall

 5. Build motmot_ros::

      . ~/motmot-ros-devel/setup.sh
      rosmake motmot_ros --rosdep-install

