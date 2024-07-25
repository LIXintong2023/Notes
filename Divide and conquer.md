This file introduces the norm and recursion of **Divide and Conquer** algorithm, and also includes a brief summary of the **Master Theorem**.
# Norm 
According to _Introduction to Algorithms_, the utilization of **Divide and Conquer** contains three steps:

1. Divide the problem into a number of subproblems that are smaller instances of the same problem.

2. Conquer the subproblems by solving them recursively. If the subproblem sizes are small enough, however, just solve the subproblems in a straightforward manner.

3. Combine the solutions to the subproblems into the solution for the original problem.

Take **Merge and sort** as an example, the three steps can be expressed as:

1. Split the original problem into two smaller sub-problems.

2. Solve the sub-problems recursively. When the sub-problem is small enough (when there is only one element in the array), it can be solved at once (naturally ordered).

3. Merge the solutions to the sub-problems (the sorted sub-arrays) into the solution to the original problem.

# Recursion
Recursive can be used to characterize the time complexity of the algorithm. The general formula of recursion is given by:
Assume that the original problem is decomposed into $a$ sub-problems, and the size of each sub-problem is $1/b$ of the original problem. The time required to solve a problem of size $n/b$ is $T(n/b)$, thus it takes $aT(n/b)$ to solve $a$ sub-problems. If the time required to decompose the problem is $D(n)$, and the time required to merge the solutions of the subproblems into the solution of the original problem is $C(n)$, then the recursive formula is:

$T(n)=aT(n/b)+D(n)+C(n)$

For **Merge and sort**, we have $a=b=2$ since we at each time divide the original problem into two subproblems and the size reduces to half of the original problem after each division. The time required to decompose the problem is $\Theta (1)$, and the time required to merge the solutions of the subproblems is $O (n)$ ($n$ is the size of the original problem). Hence, we derive the equation $T(n)=2T(n/2)+O (n)$. 

# Using recursion tree to solve the recursion
Let us take **Merge and sort** as an example.
For **Merge and sort** recursion tree, we have the equation $T(n)=2T(n/2)+O (n)$, which means, we generate the workload of $O (n)$ after each division. Since we at each time divide the original problem into two subproblems, we need $k=\log_2 n$ steps to obtain $n$ arrays with the individual size of 1. In the recursion tree, the root of the tree is the time to merge two sorted arrays of size $n/2$, while the total amount of layers of the tree is $\log_2 n$. Therefore, the time complexity of **Merge and sort** is $O (n\log n)$.

# the Master Theorem
The **Master Theorem** conserns recurrence relations of the following form:

$T(n)=aT(n/b)+f(n)$ 
where $a\geq 1$, $b>1$.
$f(n)$ is the cost of the workload outside the recursive calls, which includes the cost of dividing the problem and the cost of merging the solutions to the subproblems. Other symbols have the same meaning as above. 

Recurrences of this form often satisfy one of the three following regimes, based on how the work to split/recombine the problem $f(n)$ relates to the critical exponent $c_{crit} = \log_b a$.

_Case 1_: If $f(n)=O (n^c)$ where $c<\log_b a$, then $T(n)=\Theta (n^{\log_b a})$.

_Case 2_: If $f(n)=\Theta (n^{c_{crit}}log^k n)$ where $k\geq 0$, then $T(n)=\Theta (n^{c_{crit}}log^{k+1} n)$.

_Case 3_: If $f(n)=\Omega (n^c)$ where $c>\log_b a$, and if the regularity condition holds (see _Introduction to Algorithms_), then $T(n)=\Theta (f(n))$.

We can determine which case it is by comparing the values of $a$, $b$ and $c$.
