netft_utils
======

## WIKI: 
- http://wiki.ros.org/netft_utils


## Description
- C++ class and ROS node for ATI force/torque sensors connected to a Netbox. Includes gravity compensation and transformations.

## Set the sensor
- Input 192.168.1.84 into the address of the browser, and it will turn to the setting page.

## Preparation
- Clone and build the project.

```bash
cd ~/catkin_ws/src
git clone https://github.com/robot-chenwei/netft_utils.git
```

- Bulid it

```bash
cd ..
catkin_make --pkg netft_utils
```

## Check that it runs

```bash
roscore
rosrun netft_utils netft_utils_sim
rostopic echo /netft_data
```

## Launch a F/T Sensor node

```bash
rosrun netft_utils netft_node 192.168.1.84
rostopic echo /netft_data
```
- data type: geometry_msgs/WrenchStamped

