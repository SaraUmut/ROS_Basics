In this file you will learn the following:
* creating workspace
* creating ROS package
* creating ROS node
---------------------

1. **catkin workspace**: create a workspace, catkin is the official build system for ROS, it is needed to build ROS applications.

    1. go to Home directory by typing in terminal) `cd`
    2. create a folder: `mkdir catkin_ws`
    3. `cd catkin_ws`
    4. `mkdir src`
    5. `catkin_make`
    6. `cd devel` then `source setup.bash`
    7. add it to the bashrc file:  `vim ~/.bashrc` then add this line to the end of the file `source ~/catkin_ws/devel/setup.bash`
