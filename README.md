# Using Gmapping with Ouster LIDAR Sensor
This software was used to enable gmapping with the Ouster LIDAR sensor

To interface with the Ouster sensor using ROS see [here] (https://github.com/ouster-lidar/ouster_example/tree/master/ouster_ros)

Launching the ouster sensor is done using:
```bash
roslaunch ouster_ros os1.launch os1_hostname:=<os1_hostname> os1_udp_dest:=<udp_data_dest_ip>
```

Launching the pointcloud to laserscan conversion package, run in your terminal:
```bash
roslaunch pointcloud_to_laserscan convert1.launch
```

Our goal with this is to convert the pointcloud reading from the LIDAR sensor to a single laser scan which is fed into the Gmapping package. Gmapping takes a ```scan``` parameter as the main sensor input.

If you have any questions, please send an email to: melmzagh@stevens.edu and I can edit the documentation a bit better.
