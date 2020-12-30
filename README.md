# Motion-Planning for Autonomous driving

## 1. Objective
In this project, i have designed a Motion Planning approach based on Self-driving specilization course and implemented correspond algorithm using Python. The approach is simulated and tested in Carla simulaitor, which is a solid and modificable opensource project aiming to make it easy for autonomous-driving test/simulation in complex and various situations.

The Motion-Planning objective in this project is splited into three subtasks: behavioural planner, local planner and velocity planner. Behavioural planner is based on finite state machine. For simplicity, only simple situation is considered. That is to say, this FSM has three states: follow-lane, decelerate-to-stop and stay-stopped. Local planner has three subtasks: goal state set generation, path optimization for different goal state candidates and collision checking. In this step, local planner gives the optimal collision-free path and discretizes this path by generating a set of sequential waypoints in global frame/coordinate system. Velocity planner generates corresponding reference velocity according to the discretized sequential waypoints.

### Motion Planning in the case of obstacle avoidance
![](image/Static%20Obstacle%20Avoidance%20Capture.gif)

### Motion Planning in the case of stop sign
![](image/State%20Machine_Decelerate%20to%20stop%20Capture.gif)
![](image/State%20Machine_Decelerate%20to%20stop.gif)

## 2. Brief introduction for different subsystems

### 2.1 Behavioural Planner
![](image/Finite%20State%20Machine.jpeg)

### 2.2 Local Planner
<img src="image/Local%20Planner.jpeg" width ="400">

### 2.3 Velocity Planner
#### Use simple ramp velocity profile
<img src="image/Ramp1.PNG" width ="400"> <img src="image/Ramp2.PNG" width ="400">
#### Use trapezoidal profile