In this file you will learn the following:
* create a workspace
* creat a ROS package
* create a ROS node
---------------------

**I- Create a workspace**: create a catkin workspace. catkin is the official build system for ROS, it is needed to build ROS applications.

1. go to Home directory by typing in terminal: `cd`
2. create a folder: `mkdir catkin_ws`
3. `cd catkin_ws`
4. `mkdir src`
5. `catkin_make`
6. `cd devel` then `source setup.bash`
7. add it to the bashrc file:  `vim ~/.bashrc` then add this line to the end of the file `source ~/catkin_ws/devel/setup.bash`
  * note: or you can simply add it by typing: `echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc`

---------------------

**II- Create a ROS package**: You need to create a package to run code with ROS. Packagaes allow you to seperate code into reasonable blocks (e.g. camera package, motion planning package,.. etc.)

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

**III- Create a ROS node**: 
* The node is a process that perform computational. 
* You can create as many nodes as you want inside packages (e.g. inside Camera package: camera driver node, Image processing node ... etc.)
* Nodes communicate with each others trough topics, services, and parameter server
* Nodes can be written in Python, C++,...
* Nodes can not have the same name.

---------------------
**III-A Create a ROS node - Python**: 

1. `cd catkin_ws/src/first_pkg`
2. `mkdir scripts` where you will put your Python code file
3. `cd scripts`
4. `touch first_node.py` create python file
5. `chmod +x first_node.py` make it executable
6. edit the file `vim first_node.py` 
7. write the following:

```
!/usr/bin/env python

import rospy

if __name__='__main__':
        rospy.init_node('first_python_node') # can be different or similar to the name of the file

        rospy.loginfo("This node has been started") # print some info

        rospy.sleep(1) # sleep for 1 second

        rospy.loginfo("Exit now")
```

9. 

