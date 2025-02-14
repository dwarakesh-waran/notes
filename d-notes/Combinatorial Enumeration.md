Topic: [[My Learning]], [[Recursion]]

### What is a Combinatorial Enumeration?
Its a technique to find out the number of ways to arrange a set of objects.
### Algorithm Thinking:
Recursion usually uses a bottom up approach of solving a problem. You are delegating a work to a worker node and each worker node delegates the work to their worker node until it hits the base node.
Each worker node will do a set of steps and returns the results to its manager node. So, worker to manager - hence bottom up approach.

WORKER WORKS -> GIVES RESULT TO MANAGER -> MANAGER USES THE RESULT PROVIDED BY THE WORKER TO PROVIDE THE FINAL RESULT (BOTTOM UP)

But here, the manager node does some work and gives the result to the worker node. Then the worker node uses the result provided by the manager node and works it to provide the final result.

MANAGER WORKS -> GIVES RESULT TO WORKER -> WORKER USES THE RESULT PROVIDED BY THE MANAGER TO PROVIDE THE FINAL RESULT (TOP DOWN)