# Norm 
According to _Introduction to Algorithms_, the utilization of divide and conquer contains three steps:

1、Divide the problem into a number of subproblems that are smaller instances of the same problem.

2、Conquer the subproblems by solving them recursively. If the subproblem sizes are small enough, however, just solve the subproblems in a straightforward manner.

3、Combine the solutions to the subproblems into the solution for the original problem.

Take Merge and sort as an example, the three steps can be expressed as:

1. Split the original problem into two smaller sub-problems.

2. Solve the sub-problems recursively. When the sub-problem is small enough (when there is only one element in the array), it can be solved at once (naturally ordered).

3. Merge the solutions to the sub-problems (the sorted sub-arrays) into the solution to the original problem.

# Recursion
