# ROS 2 TurtleBot Control Project

## Description
This project implements a Docker-based ROS 2 Humble system for controlling a TurtleBot3 robot in simulation.
The robot is controlled using user input published on the `/clicked_point` topic.

## Features
- Dockerized ROS 2 Humble environment
- Custom Python control node
- TurtleBot3 Gazebo simulation (headless)
- Click-based control logic
- Unified launch file

## How to run

### Build Docker image
```bash
docker build -t turtlebot_ros:humble -f docker/Dockerfile .

run container:
docker run -it --net=host -v $(pwd)/src:/ros2_ws/src turtlebot_ros:humble

run system:
ros2 launch turtlebot_control system.launch.py
