# Hector SLAM dengan TurtleBot3 di Gazebo

Proyek ini adalah simulasi SLAM menggunakan algoritma **Hector SLAM** dan robot **TurtleBot3** di Gazebo. Simulasi bertujuan untuk membangun peta lingkungan secara real-time dengan data lidar tanpa menggunakan odometri.

## Cara Menjalankan Simulasi

### Prasyarat
- **Ubuntu 16.04**
- **ROS Kinetic**
- **Gazebo**
- **Paket TurtleBot3 dan Hector SLAM**

**INSTALASI**
$ sudo apt-get install ros-kinetic-turtlebot3

sudo apt-get install ros-kinetic-hector-slam

**MENJALANKAN**
export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_gazebo turtlebot3_world.launch

roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=hector

**PERGERAKAN**
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**MENYIMPAN PETA**
rosrun map_server map_saver -f ~/map1
