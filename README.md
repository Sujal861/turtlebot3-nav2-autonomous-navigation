# TurtleBot3 Nav2 Autonomous Navigation in Gazebo

**Robotics Software Intern Assignment — Antropi Robotics**

This project documents a TurtleBot3 Burger simulation using ROS 2 Jazzy, Gazebo, and Navigation2 (Nav2). The assignment goal is to send the robot to a navigation goal while avoiding obstacles using the existing Nav2 stack.

## Assignment scope

- Launch TurtleBot3 in Gazebo.
- Start the Nav2 stack and RViz.
- Set or send a goal in RViz.
- Demonstrate autonomous motion and obstacle avoidance.
- Document setup, approach, challenges, and learnings.

No custom navigation algorithm is required by the assignment. The priority is configuring and demonstrating the standard navigation stack.

## Environment

- Ubuntu + ROS 2 Jazzy
- TurtleBot3 Burger
- Gazebo
- Navigation2 (Nav2)
- RViz2

## Launch example

For the standard TurtleBot3 house simulation, with the relevant TurtleBot3 and Nav2 packages installed:

```bash
source /opt/ros/jazzy/setup.bash
export TURTLEBOT3_MODEL=burger
ros2 launch turtlebot3_gazebo turtlebot3_house.launch.py
```

Launch availability and whether Nav2 is included depend on the installed package and launch file. If Gazebo opens without Nav2, start the matching TurtleBot3 Nav2 launch for your installed Jazzy packages. Use `ros2 launch turtlebot3_navigation2` to list available launch files rather than assuming a filename.

## Evidence status

The simulation and ROS topic graph have been inspected during development. The `/scan` topic was present, but continuous scan reception and successful goal-to-goal autonomous navigation have not yet been confirmed. Do not claim successful obstacle avoidance until a complete goal navigation run is recorded.

## Submission checklist

- [ ] Gazebo and RViz visible in demo
- [ ] Robot localized and map visible
- [ ] Goal sent using RViz/Nav2
- [ ] Robot reaches the goal autonomously
- [ ] Obstacle avoidance demonstrated
- [ ] 1–2 minute screen recording saved in `media/`
- [ ] Setup and troubleshooting documented
- [ ] Public GitHub repository link checked
- [ ] Submission form completed

## Repository structure

```text
.
├── README.md
├── docs/
│   ├── APPROACH.md
│   ├── REPORT.md
│   ├── TEST_PLAN.md
│   └── SUBMISSION_ANSWERS.md
└── media/
    └── README.md
```
