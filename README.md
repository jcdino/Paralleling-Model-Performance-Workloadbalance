# Comparing Performance and Workload Balance of Paralleling Models

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
### Comparing the performance with the increase of number of threads (1 to 8) with OpenMP
<img width="857" alt="image" src="https://user-images.githubusercontent.com/90415099/166249364-b03274eb-d02c-4c81-98cd-891994ff8092.png">
--> The increase in the number of threads used leads to better performamce in terms of the total computation time.

### Comparing the performance overhead with different scheduling methods (Static, Dynamic, Guided) with OpenMP
<img width="896" alt="image" src="https://user-images.githubusercontent.com/90415099/166249627-9950dc71-49a8-4542-b796-aef5cf04a663.png">

<img width="891" alt="image" src="https://user-images.githubusercontent.com/90415099/166249671-ed997436-ae85-40d3-bdcf-11e593f3d2d0.png">
--> Dynamic Scheduling had the highest overhead followed by Guided and Static. The overhead in Dynamic Scheduling occures because it checks for remaining tasks after ever iteration. Guided Scheduling also has a overhead because it is a type of Dynamic Scheduling, but it starts with large chunks of task which leads to less number of total chunks than Guided Scheduling.

### Comparing the workload balance with different scheduling methods (Static, Dynamic, Guided) with OpenMP
#### Static
<img width="872" alt="image" src="https://user-images.githubusercontent.com/90415099/166261093-f295e56d-0aee-407f-b24a-fb5f8ea2cec9.png">

#### Dynamic
<img width="872" alt="image" src="https://user-images.githubusercontent.com/90415099/166261107-155423b2-e108-4980-b7be-9a547cf61e31.png">

#### Guided
<img width="872" alt="image" src="https://user-images.githubusercontent.com/90415099/166261122-cb5743cc-5907-4aa5-82e7-973334257c2f.png">
--> Dynamic Scheduling had the best workload balance followed by Guided Scheduling and then Static Scheduling.

### Comparing the performance of baseline module, OpenMP, TBB
(From here, used a different computer enviorment due to small issues on the TBB setup which could have caused some problems)
<img width="863" alt="image" src="https://user-images.githubusercontent.com/90415099/166252577-28d57fcb-8eaf-4f50-99e2-80818da6eb68.png">

### Evaluation of the workload balance between threads using TBB
<img width="849" alt="image" src="https://user-images.githubusercontent.com/90415099/166253049-f50ea212-523e-4581-9b5e-907333c9002e.png">

