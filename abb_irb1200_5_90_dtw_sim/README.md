# Simulation DTW
Gazebo Simulation with Moveit Controls in Rviz and DTW Plot comparing simulated and theoretical trajectory

1. Install ROS Noetic [Tutorial here](https://wiki.ros.org/noetic/Installation/Ubuntu)
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt update
sudo apt install ros-noetic-desktop-full
source /opt/ros/noetic/setup.bash
```

2. Install Moveit [Tutorial here](https://moveit.ros.org/install/)
```
sudo apt install ros-noetic-moveit
```

3. Install Pandas, NumPy and DTW
```
sudo apt install python3-pip
pip install pandas dtw-python numpy
```
It is possible that numpy needs to be updated first
```
pip install --upgrade numpy
```

4. Install all the dependencies 
```
rosdep install --from-paths src --ignore-src --rosdistro noetic -y
```

5. Create a new ROS workspace
```
mkdir -p ~/yourfoldersname/src
cd ~/yourfoldersname/
catkin_make
```

6. Clone this repository into the src folder
```
cd ~/src/
git clone https://github.com/vmarquim/simulation_dtw.git
```

7. Go back to the root ot the workspace and source
```
cd ..
source devel/setup.bash
```

8. To start the Robot Simulation in Gazebo and the RViz with Moveit, Run the simulation launch file
```
roslaunch abb_irb1200_5_90_dtw_sim simulation_program.launch
```

9. Run the run and compare launch file
```
roslaunch abb_irb1200_5_90_dtw_sim run_and_compare.launch
```

10. Possible values for run_mode (default is "square")
```
"square"
"circle"
"line"
"random-valid"
```

# Connection with the real robot

here write
