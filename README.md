## How to use the lab3 launch files

#### Launch Files

- `lab3_rviz_basic.launch`
   This launch file launches rviz with the original lab3 config. Technically this is the same config file as in Lab2. This launch file also runs the bag in the specified file path.

- `lab3_rviz_laserscans.launch`
   This launch file launches rviz with the LaserScan things already setup and listening to the respective topics. It also launches the bag file spcified in the `bag_type` argument.

- `lab3_rviz_map.launch`
   This launch file launches rviz with the LaserScan things already setup and listening to the respective topics. It runs the map_server stuff and sets the base view in rviz to the map, instead of the base link of the robot. 


#### Launch File Args

- bag_type

   This argument tells the launch file the name of the bag file to run. You should place the bag file inside the folder: `lab3/src/bags/`. It defaults to the complete bag, filename: `glennan_5_complete-002.bag`

- use_xacro

   This argument tells the launch file whether to use a xacro file or the plain urdf file from lab2. Defaults to false.

- use_old_file

   This argument tells the launch file whether to use the lab2 xacro file or the lab3 xacro file. Defaults to false. If `use_xacro` is set to false and `use_old_file` is set to true, then you will get an error and the launch will crash.

- use_clock

   This argument tells ROS whether it should use an external (simulated) clock. If this argument is set to true, then ROS will use a simulated clock.

#### Launch Command

`roslaunch lab3 <LAUNCH_FILE_NAME> [ARGS]`
