#Project name: MapmyLocal SLAM project In the Workspace
#Environment: Tested on x86 + GTX1070 (6GB) Ubuntu 16.04 Linux System (non-virtual) + 16GB RAM (higher always recommended).

#Now, Steps to do:
#After all instructions are followed mentioned in Udacity project page for SLAM.
link: https://classroom.udacity.com/nanodegrees/nd209/parts/dad7b7cc-9cce-4be4-876e-30935216c8fa/modules/aec2781f-e368-4e1e-9aef-d46aeee55354/lessons/0f504827-ab9c-4280-913f-413e4df602be/concepts/c9493041-9c32-435e-a190-01c89e7b2e71 
#Here are the executable steps:

$ cd /home/workspace/catkin_ws/src$ 
$ cd..
$ catkin_make

#On Terminal 1
#Launch the turtlebot in a Willow Garage environment
$ source devel/setup.bash
$ roslaunch mapmylocal udacity_world.launch 
Turtlebot should now appear in a Kitchen & dining world environment.
$ roslaunch mapmylocal gas-stn.launch 
Turtlebot should now appear in a Kitchen & dining world environment.


#Terminal 2
#Launch the keyboard teleop node
$ cd /home/workspace/catkin_ws
$ source devel/setup.bash
$ roslaunch mapmylocal mapping.launch
The node should start registering your first scan.


#Terminal 3
#Run the slam_gmapping node
$ cd /home/workspace/catkin_ws
$ source devel/setup.bash
$ rosrun mapmylocal teleop.launch
#now, you should be able to move, perform mapping by navigation.

#Terminal 4
$ cd ~

#$ rosrun tf view_frames
#$ evince frames.pdf
