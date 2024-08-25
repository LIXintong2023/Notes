# Affine sets
## Typical affine sets
1. Solution set of a system of linear equations, i.e., $C=\{x|Ax=b\}$ (given $Ax_1=b$ and $Ax_2=b$, we have $A(\theta x_1+(1-\theta)x_2)=b$). Also note that every affine set can be expressed as the solution set of a system of linear equations.
2. A line.
3. A plane.
4. A hyper plane.
5. The empty set $\emptyset$.
# Convex sets
## Typical convex sets
1. The set of any single point.
2. The whole space of $R^n$.
3. A line: $y = \theta x_1 + (1-\theta)x_2$, $0\leq \theta \leq 1, \theta \in R^n$.
4. A line segment: $y = \theta x_1 + (1-\theta)x_2$, $0\leq \theta \leq 1, \theta \in R^n$.
5. The empty set $\emptyset$.
# Cones
## Typical cones
1. $n$ rays starting from the origin.
2. Infinite rays starting from the origin (consist of a convex cone).
3. origin (a single point not in origin is not a cone).
4. The empty set $\emptyset$ (and also a convex cone).
# Comparison of concepts
$\sum_{k=1}^K \theta_k x_k$ is a
1. Affine combination: if $x_1, x_2,..., x_k \in C, \sum_{k=1}^K \theta_k =1$.
2. Convex combination: if $x_1, x_2,..., x_k \in C, \sum_{k=1}^K \theta_k =1, \forall \theta_k \in [0,1]$.
3. Convex conic combination: if $x_1, x_2,..., x_k \in C, \forall \theta_k >0$.
# Typical convex functions
1. Indicator function: $\widetilde{I_c} (x) = \lbrace 0 \qquad if \quad x \in C, +\infty \qquad if \quad x \not\in C \rbrace$.

   $\widetilde{I_c} (x)$ 's domain C is a convex set, and the function $f(x)+\widetilde{I_c} (x)$ equals $f(x)$ if $f$ is restricted to the set C.

   If we chcange $+\infty$ into $-\infty$, $\widetilde{I_c} (x)$ becomes a concave function.

2. Infimum and Supremum
   Infimum: 
