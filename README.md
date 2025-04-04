# CPU Scheduling Project

![Screenshot 2025-04-03 at 8 03 44 PM](https://github.com/user-attachments/assets/b51aea45-a3df-4994-a810-a775a1343561)



A simple C++ implementation of a Priority-based CPU Scheduling algorithm developed in Ubuntu Linux.

## Overview

This project simulates a priority-based CPU scheduling algorithm. It manages 5 processes, scheduling them based on their priorities. The process with the highest priority value gets executed first, and during execution, its priority decreases.

## Features

- Simulates 5 concurrent processes
- Priority-based scheduling algorithm
- Process Control Block (PCB) implementation
- Interactive visualization of process states and execution
- Process states include:
  - 'R' - Ready
  - 'r' - Running
  - 'F' - Finished/Terminated

## How It Works

1. The program initializes 5 Process Control Blocks (PCBs)
2. User inputs ID, priority and runtime for each process
3. The scheduler selects the process with highest priority to run
4. During execution:
   - A running process has its priority decreased by 1 each cycle
   - Runtime is decreased by 1 each cycle
   - When runtime reaches 0, the process is marked as finished
   - The scheduler then selects the next highest priority process

## Compilation and Execution

To compile the program in Ubuntu Linux:

```bash
g++ CPU-Scheduling.cpp -o cpu_scheduler
```

To run the program:

```bash
./cpu_scheduler
```

## Input Format

For each process, you'll be prompted to enter:
- Process ID (a character)
- Priority (integer)
- Runtime (integer)

Example input for a single process:
```
A       10      5
```
This creates a process with ID 'A', priority 10, and runtime 5.

## Output

The program displays the status of all processes after each execution step, showing:
- Process ID
- Current priority
- Remaining runtime
- Current state (R: Ready, r: Running, F: Finished)

## What I Learned

Through this project, I gained valuable insights into:

- The fundamentals of operating system process scheduling algorithms
- Implementation of priority-based scheduling and its behavior
- Process state management (Ready, Running, Terminated)
- Practical application of Process Control Block (PCB) data structures
- Interactive user input handling and process simulation
- Dynamic process priority adjustment during execution

## Difficulties Faced

Some challenges I encountered during this project:

1. Properly implementing the scheduling algorithm logic to select the highest priority process
2. Managing the state transitions between Ready, Running, and Finished states
3. Ensuring correct priority and runtime decrementing during execution
4. Handling edge cases when multiple processes had the same priority
5. Designing an intuitive display for showing process status after each execution step

## How I Overcame Challenges

I employed several strategies to overcome these difficulties:

1. Drew state diagrams to visualize the process transitions before implementing them in code
2. Used incremental development, implementing and testing one feature at a time
3. Added detailed comments to keep track of the algorithm logic
4. Created test cases with different process configurations to verify the scheduler's behavior
5. Consulted operating systems literature to better understand priority-based scheduling concepts
6. Collaborated with classmates to discuss alternative approaches and solutions
7. Implemented debugging output to track the internal state during execution

## Environment

This project was developed and tested on Ubuntu Linux.

## Author
Bernard Ginn
