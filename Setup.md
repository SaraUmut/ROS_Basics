# How to set up your workstation to work with ROS

Firstly you should setup Ubuntu and ROS, by following the steps below:
(Note: I will work with Ubunut 16.04 (Xenial) and ROS Kinetic)

**I- Ubunut:**

1. Download the ios:
https://releases.ubuntu.com/16.04/
(direct link to download Ubunut on 64-bit system: https://releases.ubuntu.com/16.04/ubuntu-16.04.7-desktop-amd64.iso)

2. Create a bootable USB stick on Ubuntu
https://ubuntu.com/tutorials/create-a-usb-stick-on-ubuntu#3-launch-startup-disk-creator

OR, on Windows:
https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview

3. Boot from the USB and download Ubuntu and restart

4. In Ubuntu: open "Software Updater" and make an update then restart.

5. Update & upgrade packages:
    1. update: (write in terminal) `sudo apt-get update`
    2. upgrade: (terminal) `sudo apt-get upgrade`
    
6. Install some useful packages:
    1. `sudo apt install build-essential gcc make perl dkms`
    2. vim editor: `sudo apt install vim`
    3. `sudo apt-get update`
    4. `sudo apt-get upgrade`
    
**II- Ubunut:**

1. Follow the steps in the official link: http://wiki.ros.org/kinetic/Installation/Ubuntu
   (use the Desktop-Full Install version).
   
2. Ensure that the ROS environment variables are added to your bash file, by:
    1. type: `vim ~/.bashrc`
    2. go to the end of the file and you should find the line: `source /opt/ros/kinetic/setup.bash` written.
    3. if not, add it by going to insert mode first (press i) then write the previous line. Save and exit (Esc : wq)
    
3. check the installation by typing (in terminal): `printenv | grep ROS`
   (you should get some information about the ROS path like: ROS_ROOT= /opt/ros/kinetic/share/ros)
        
4. check that ROS master can run correctly, by typing: `roscore`


**Useful links:**
1. ROS Distribuations: http://wiki.ros.org/Distributions
2. To download Ubunutu & ROS on virtual Machine, I recommend using 'Virtual Box': https://www.virtualbox.org/wiki/Downloads
3. ROS course: https://www.udemy.com/course/ros-for-beginners
