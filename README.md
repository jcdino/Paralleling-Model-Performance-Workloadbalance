# Comparing Performance and Workload Balance of paralleling Moduels
## Content
1. [Problem Description](Problem-Description)
2. [Parallel Programming Modules](Parallel-Programming-Modules)
3. [Results](Results)

## Problem Description
### BFS (Breadth First Search)

## Parallel Programming Modules

### OpenMP
- Historically used for loop-level and regular parallelism through its compiler directives
-  From OpenMP 3.0, supports task parallelism

### CILK Plus
- Provides language contrasts for both task and data parallelism
- Simple and High level of abstraction 
- Scheduling policy provides load balance close to the optimal
- Deprecated in 2018

### Thread Building Blocks (TBB)
- Object C++ runtime library 
- Contains data structures and algorithms used in parallel programs
- Abstracts the low-level thread interface

## Results

### BFS
#### Comparing the performance with the increase of number of threads (1 to 8) with OpenMP
<img width="857" alt="image" src="https://user-images.githubusercontent.com/90415099/166249364-b03274eb-d02c-4c81-98cd-891994ff8092.png">

#### Comparing the workload balance with different scheduling methods (Static, Dynamic, Guided) with OpenMP
<img width="896" alt="image" src="https://user-images.githubusercontent.com/90415099/166249627-9950dc71-49a8-4542-b796-aef5cf04a663.png">

<img width="891" alt="image" src="https://user-images.githubusercontent.com/90415099/166249671-ed997436-ae85-40d3-bdcf-11e593f3d2d0.png">

#### Comparing the performance of baseline module, OpenMP, TBB
<img width="863" alt="image" src="https://user-images.githubusercontent.com/90415099/166252577-28d57fcb-8eaf-4f50-99e2-80818da6eb68.png">

#### Evaluation of the workload balance between threads using TBB
<img width="849" alt="image" src="https://user-images.githubusercontent.com/90415099/166253049-f50ea212-523e-4581-9b5e-907333c9002e.png">

