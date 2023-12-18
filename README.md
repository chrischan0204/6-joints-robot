# Kinematic Problem Solver for 6-Axis Collaborative Robot

This repository contains a solution for the kinematic forward problem of a 6-axis collaborative robot's DH-model. The goal of this project is to calculate the end-effector position in the Cartesian coordinate system.

## Table of Contents
- [Kinematic Problem Solver for 6-Axis Collaborative Robot](#kinematic-problem-solver-for-6-axis-collaborative-robot)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Algorithm](#algorithm)
  - [Compilation and Execution](#compilation-and-execution)
  - [Requirements](#requirements)
  - [Usage](#usage)
  - [LICENSE](#license)

## Description
The project involves implementing an algorithm to solve the kinematics problem for a DH-model 6-axis collaborative robot. The goal of this project is to calculate the end-effector position in the Cartesian coordinate system. The DH parameters for the robot's joints are provided in the table below:

| Joint    | theta (deg) | a (m) | d (m)      | alpha (rad) |
|----------|-------------|-------|------------|-------------|
| Joint 0  | 10          | 0     | 0.21       | π/2         |
| Joint 1  | -50         | -0.8  | 0.193      | 0           |
| Joint 2  | -60         | -0.598| -0.16      | 0           |
| Joint 3  | 90          | 0     | 0.25       | π/2         |
| Joint 4  | 50          | 0     | 0.25       | -π/2        |
| Joint 5  | 0           | 0     | 0.25       | 0           |

## Algorithm

The algorithm for solving the forward kinematics problem can be described in English as follows:

1. Initialize the joint angles or joint variables of the robot arm.
2. Define the transformation matrices for each link of the robot arm.
3. Create a transformation chain by multiplying the transformation matrices from the base link to the end effector.
4. Apply the Denavit-Hartenberg (DH) parameters for each link to calculate the transformation matrix.
5. Calculate the position and orientation of the end effector based on the final transformation matrix.
6. Display or use the obtained end effector position and orientation as required.

## Compilation and Execution

The project can be compiled and executed on a Linux operating system. The recommended programming languages for implementation are C for console applications.

To compile and run the console application:

```bash
make clean && make
make run
```

## Requirements

- GCC (for C implementation)

## Usage

1. Run the compiled executable.
2. Input the desired theta.
3. The algorithm will calculate and display end-effector position for the robot.

## LICENSE
This project is licensed under the [MIT LICENSE](LICENSE).
