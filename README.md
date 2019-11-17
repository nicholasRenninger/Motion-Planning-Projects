# Motion Planning Projects
A repo containing all of my motion planning algorithm projects.


## Tool Class Hierarchy
This diagram shows the notional, evolving class design for the underlying project framework:
<img src="https://github.com/nicholasRenninger/Motion-Planning-Projects/blob/master/classHierarchyDiagram.png"/>


## [bugAlgorithms_and_kinematics](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics)

This repo contains implementations of Bug Algorithms and a Forwards / Inverse Kinematics solver for a 3-link manipulator. 

Results of the implentation include:

* plots of the path performance of the different **bug planning algorithms** on multiple environments
* plots of the results of running **forwards / inverse kinematics on a user specified 2-link manipulator**

Bug 1 Algorithm           |  Bug 2 Algorithm          | 3-Link Manipulator 
:-------------------------:|:-------------------------:|:-----:
![](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics/blob/master/figures/bug_scenario1-bug1.png)   |  ![](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics/blob/master/figures/bug_scenario1-bug2.png)| ![](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics/blob/master/figures/manipulator_scenario1-forward_kin_0.785_1.57_-0.524.png)

## [cSpaceViz_Gradient_Wavefront_planners](https://github.com/nicholasRenninger/cSpaceViz_Gradient_Wavefront_planners)

Implementation of a 2-D 2DoF manipulator configuration space visualizer, as well as implementations of a gradient descent and wavefront planner for this manipulator. 

Results of the implentation include:

* **C-Space visualizer for a translating, rotating robot and obstacle** of the same polygonal shape
* **Gradient descent planner** path visualization for a point robot in multiple enviroments, including those from the [bugAlgorithms_and_kinematics](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics) repo.
* **Wavefront planner** path visualization for a point robot in multiple enviroments, including those from the [bugAlgorithms_and_kinematics](https://github.com/nicholasRenninger/bugAlgorithms_and_kinematics) repo.
* **C-Space visualizer for a 2-link manipulator** with arbitrary polygonal obstacles
* **Wavefront planner** workspace path for the 2-link manipulator

2-Link Manipulator Plan Viz.           |  2-Link Manipulator C-Space          | Potential Gradient Planner
:-------------------------:|:-------------------------:|:-----:
![](https://github.com/nicholasRenninger/cSpaceViz_Gradient_Wavefront_planners/blob/master/figures/manipulator_env3-workspace.png)   |  ![](https://github.com/nicholasRenninger/cSpaceViz_Gradient_Wavefront_planners/blob/master/figures/manipulator_env3-wavefrontPlannerwavefront.png)| ![](https://github.com/nicholasRenninger/cSpaceViz_Gradient_Wavefront_planners/blob/master/figures/gradient_env2-gradientPlanner.png)

## [AStar_and_PRM_Planning_Analysis](https://github.com/nicholasRenninger/AStar_and_PRM_Planning_Analysis)

Implementation of the A* and Dijkstra optimal graph search algorithms, a Fast Probabilistic Roadmap (PRM) Planner with path smoothing, and a benchmarking suite for doing parametric performance evaluation of the planners modules. 

Built with a `networkx` Graph backbone and library implementations of:
* Set-Priority Queue (based on `heapq`)
* KDTree (based on `cKDTree`)
* Union-Find (based on `newtorkx.util`)

ADTs for speed.

Results of the imlementation include:

* Visualization and implementation of the **A* and Dijkstra Optimal Search Algorithms**
* **Smoothing PRM Planner** path visualization for a point robot in multiple enviroments, including those from the [cSpaceViz_Gradient_Wavefront_planners](https://github.com/nicholasRenninger/cSpaceViz_Gradient_Wavefront_planners) repo.
* **Benchmarking and statistical analysis / visualization** of the Smoothing PRM Planner in multiple enviroments, with the ability to do parametric studies of planner parameters.

PRM Planner           |  Path Length Benchmarking          | Computation Time Benchmarking
:-------------------------:|:-------------------------:|:-----:
![](https://github.com/nicholasRenninger/AStar_and_PRM_Planning_Analysis/blob/master/figures/prmPointRobot_env2-PRM%20-%20path%20length%20%3D%2015.8%20%20n%20%3D%20250%20%20r%20%3D%202.png)   |  ![](https://github.com/nicholasRenninger/AStar_and_PRM_Planning_Analysis/blob/master/figures/prmPointRobotBenchmark_env1-pathLength-PRM_stats.png)| ![](https://github.com/nicholasRenninger/AStar_and_PRM_Planning_Analysis/blob/master/figures/prmPointRobotBenchmark_env3-computationTimeInSeconds-PRM_stats.png)
