In this file you will learn the following:
* create a workspace
* creat a ROS package
* create a ROS node
---------------------

**create workspace**: create a catkin workspace. catkin is the official build system for ROS, it is needed to build ROS applications.

1. go to Home directory by typing in terminal: `cd`
2. create a folder: `mkdir catkin_ws`
3. `cd catkin_ws`
4. `mkdir src`
5. `catkin_make`
6. `cd devel` then `source setup.bash`
7. add it to the bashrc file:  `vim ~/.bashrc` then add this line to the end of the file `source ~/catkin_ws/devel/setup.bash`
  * note: or you can simply add it by typing: `echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc`

---------------------

**create a ROS package**: You need to create a package to run code with ROS. Packagaes allow you to seperate code into reasonable blocks (e.g. camera package, motion planning package,.. etc.)

1. `cd catkin_ws/src`
2. `catkin_create_pkg first_pkg roscpp rospy std_msgs`
 * It will create a package with the name 'first_pkg' 
 * and give it the following dependencies: 
 * roscpp: C++ ROS library, which allows you to run ROS functionality in your C++ code)
 * rospy: Python ROS library
 * std_msgs: 
     
3. check that in `cd catkin_ws/src/first_pkg` you have 'CMakeLists.txt' and inside it you have the name of the package and its dependencies (`vim CMakeLists.txt`).
4. check the 'package.xml' too (`vim package.xml`)
5. `cd ~/catkin_ws/` then `catkin_make` 

---------------------

**create a ROS node**:
