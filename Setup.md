# How to set up your workstation to work with ROS

Firstly you should setup Ubuntu and ROS, by following the steps below:
(Note: I will work with Ubunut 16.04 (Xenial) and ROS Kinetic)

**I- Ubunut:**

1- Download the ios:
https://releases.ubuntu.com/16.04/
(direct link to download Ubunut on 64-bit system: https://releases.ubuntu.com/16.04/ubuntu-16.04.7-desktop-amd64.iso)

2- Create a bootable USB stick on Ubuntu
https://ubuntu.com/tutorials/create-a-usb-stick-on-ubuntu#3-launch-startup-disk-creator

OR, on Windows:
https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview

3- Boot from the USB and download Ubuntu and restart

4- In Ubuntu: open "Software Updater" and make an update then restart.

5- update & upgrade packages:
    A. update: (write in terminal) `sudo apt-get update`
    B. upgrade: (terminal) `sudo apt-get upgrade`
    
6- install some useful packages:
    A. `sudo apt install build-essential gcc make perl dkms`
    B. vim editor: `sudo apt install vim`
    C. `sudo apt-get update`
    D. `sudo apt-get upgrade`
    
**II- ROS:** Download ROS Kinetic:
    1. follow the steps in the official link: http://wiki.ros.org/kinetic/Installation/Ubuntu
       (use the Desktop-Full Install version).
    2. check the installation by typing (in terminal): `printenv | grep ROS`
        (you should get some information about the ROS path like: ROS_ROOT= /opt/ros/kinetic/share/ros)


**Useful links:**
1- ROS Distribuations: http://wiki.ros.org/Distributions
2- To download Ubunutu & ROS on virtual Machine, I recommend using 'Virtual Box': https://www.virtualbox.org/wiki/Downloads
