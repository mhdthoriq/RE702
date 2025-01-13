# Hector SLAM dengan TurtleBot3 di Gazebo

Proyek ini adalah simulasi SLAM menggunakan algoritma **Hector SLAM** dan robot **TurtleBot3** di Gazebo. Simulasi bertujuan untuk membangun peta lingkungan secara real-time dengan data lidar tanpa menggunakan odometri.
# Demo by Muhammad Thoriq Mubarak [4222111004]

## Cara Menjalankan Simulasi

### Bahan
- **Ubuntu 16.04**
- **ROS Kinetic**
- **Gazebo**
- **Paket TurtleBot3 dan Hector SLAM**

**INSTALASI**
```bash
sudo apt-get install ros-kinetic-turtlebot3
```
```bash
sudo apt-get install ros-kinetic-hector-slam
```

**MENJALANKAN**
```bash
export TURTLEBOT3_MODEL=waffle_pi
```
```bash
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
```bash
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=hector
```

**PERGERAKAN**
```bash
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

**MENYIMPAN PETA**
```bash
rosrun map_server map_saver -f ~/map1
```
<img width="560" alt="image" src="https://github.com/user-attachments/assets/4a14fe6d-daad-439c-882b-19e17e0854b9" />


