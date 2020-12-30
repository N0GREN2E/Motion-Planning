# Motion-Planning for Autonomous driving

### 1. Objective
In this project, i have designed a Motion Planning approach based on Self-driving specilization course and implemented correspond algorithm using Python. The approach is simulated and tested in Carla simulaitor, which is a solid and modificable opensource project aiming to make it easy for autonomous-driving test/simulation in complex and various situations.

The Motion-Planning objective in this project is splited into three subtasks: behavioural planner, local planner and velocity planner. Behavioural planner is based on finite state machine. For simplicity, only simple situation is considered. That is to say, this FSM has three states: follow-lane, decelerate-to-stop and stay-stopped. Local planner has three subtasks: goal state set generation, path optimization for different goal state candidates and collision checking. In this step, local planner gives the optimal collision-free path and discretizes this path by generating a set of sequential waypoints in global frame/coordinate system. Velocity planner generates corresponding reference velocity according to the discretized sequential waypoints.

### Motion Planning in the case of obstacle avoidance
![](Static%20Obstacle%20Avoidance%20Capture.gif)