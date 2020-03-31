# ball_chaser

This repo contains a simulation environment of a mobile robot and a white ball to chase. my_robot creates the simulation environment with additional plugins. my_robot also ensures the ROS communication with Gazebo and launches the RViz. There is also ball_chaser package which is responsible to drive the robot and process the image w.r.t the camera on robot.
### Directory Structure
```
    Go Chase It                        # Go Chase It Project
    ├── my_robot                       # my_robot package
    │   ├── launch                     # launch folder for launch files
    │   │   ├── robot_description.launch
    │   │   ├── world.launch
    │   ├── meshes                     # meshes folder for sensors
    │   │   ├── hokuyo.dae
    │   ├── urdf                       # urdf folder for xarco files
    │   │   ├── my_robot.gazebo
    │   │   ├── my_robot.xacro
    │   ├── world                      # world folder for world files
    │   │   ├── <yourworld>.world
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info
    ├── ball_chaser                    # ball_chaser package
    │   ├── launch                     # launch folder for launch files
    │   │   ├── ball_chaser.launch
    │   ├── src                        # source folder for C++ scripts
    │   │   ├── drive_bot.cpp
    │   │   ├── process_images.cpp
    │   ├── srv                        # service folder for ROS services
    │   │   ├── DriveToTarget.srv
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info
    └──
    └── 
```

### Steps to launch the simulation

#### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

#### Step 2 Clone the lab folder in /home/workspace/
```sh
$ cd /home/user/ros_catkin_ws_dir/src/
$ git clone https://github.com/canersu/ball_chaser.git

#### Step 3 Compile the code
```sh
$ cd /home/user/ros_catkin_ws_dir/
$ catkin_make
```

#### Step 4 Running the code
```sh
$ roslaunch my_robot world.launch
$ roslaunch ball_chaser ball_chaser.launch
```
