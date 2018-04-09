# px4_mavros_and_sitl
## Problem 1

You need to write a high-level controller using this topic in [mavros](https://dev.px4.io/en/ros/mavros_offboard.html) node
```shell
 pose.pose.position.x
 pose.pose.position.y
 pose.pose.position.z
 ```
 that will perform tracking of sinusoidal ```like: y=sin(x)``` using given block diagram 

![alt text](https://raw.githubusercontent.com/AerialRobotics-IITK/practice/master/px4_mavros_and_sitl/a1.png?raw=true )

* Note that if find any difficluties in [Gazebo](https://dev.px4.io/en/simulation/ros_interface.html) then try with [jmavsim](https://dev.px4.io/en/simulation/jmavsim.html)


#
#

## Problem 2

You all have developed a basic knowledge of control system stack of our framework (after doing problem #1). 
So  now you have perform a trajectory tracking task using given data of the desired trajectory   ```s_des.npy``` using an *PD* controller on position

ROS Topic~ ```/mavros/local_position/pose``` provide you data of UAV current location in (x,y,z).</br>
File ```s_des.npy``` provide you desired position that needs to achieved.
So apply an PD controller on these things and generate ```attitude setpoints``` and this will do the this task!

```python
# s_des.npy need to be read by a python script 
# It contains 2-D array of data so you will have to use just first row for x, second row for y, third row for z.
# if it not work out let me know!
```

###### Note: These files   [mc_pos_control](https://github.com/AerialRobotics-IITK/Firmware/blob/master/src/modules/mc_pos_control/mc_pos_control_main.cpp#L260) and [this](https://github.com/harshsinh/warehouse-quad/blob/master/controller/src/controller.cpp) and File ```mc_pos_control_main.cpp``` can help if you want!
