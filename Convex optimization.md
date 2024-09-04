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
1. Indicator function:

   $\widetilde{I_c} (x) = \lbrace 0 \qquad if \quad x \in C, +\infty \qquad if \quad x \not\in C \rbrace$.

   $\widetilde{I_c} (x)$ 's domain C is a convex set, and the function $f(x)+\widetilde{I_c} (x)$ equals $f(x)$ if $f$ is restricted to the set C.

   If we chcange $+\infty$ into $-\infty$, $\widetilde{I_c} (x)$ becomes a concave function.

2. Infimum and Supremum
   
   **Infimum**: infimum (abbreviated **inf**) of a subset **$S$** of a partially ordered set **$P$** is the greatest element in **$P$** that is less than or equal to each element of **$S$** if such an element exists. If the infimum of **$S$** exists, it is unique, and if $b$ is a lower bound of **$S$**, then $b$ is less than or equal to the infimum of **$S$**. Consequently, the infimum is commonly referred to as the greatest lower bound (abbreviated as GLB).
   
   **Supremum**: supremum (abbreviated **sup**) of a subset **$S$** of a partially ordered set **$P$** is the least element in **$P$** that is greater than or equal to each element of **$S$** if such an element exists. If the supremum of **$S$** exists, it is unique, and if $b$ is an upper bound of **$S$**, then the supremum of **$S$** is less than or equal to $b$. Consequently, the supremum is also referred to as the least upper bound (or LUB).
   
   Note: The infimum or supremum of a subset can be outside the subset, the set that contains the infimum or supremum (i.e. the partially ordered set  **$P$**) can be the $(-\infty, +\infty)$, 

   An example: For the subset $M=[1,2]$ and set $P=R$, we have ${\rm max} (M)=2, {\rm min} (M)=1$, and ${\rm sup}(M)=2, {\rm inf}(M)=1$, while for the set $M=(1,2)$, we do not have lower bound and upper bound of $M$, (i.e. ${\rm max}(M)={\rm None}, {\rm min}(M)={\rm None}$), but have ${\rm sup}(M)=2, {\rm inf}(M)=1$.

3. $f(x)=-log(x)$
4. Linear functions
5. Piecewise linear functions
6. If $f(x)$ is convex, define $g(x)=(c^Tx+d)f((Ax+b)/(c^Tx+d))$, ${\rm dom} (g)=\lbrace x|c^Tx+d>0, ((Ax+b)/(c^Tx+d)) \in {\rm dom} (f)\rbrace$, then $g(x)$ is convex.
# Typical quasiconvex functions
## Definition
1. A function $f$: $R^n \rightarrow R$ is called quasiconvex (or unimodal) if its domain and all its sublevel sets\\
   $S_\alpha = \lbrace x \in {\rm dom}f|f(x)\leq \alpha\rbrace$, for $\alpha \in {\rm R}$, are convex.
   A function that is both quasiconvex and quasiconcave is called quasilinear.
   If a function $f$ is quasilinear, then its domain, and every level set $\lbrace x | f(x)= \alpha\rbrace $ is convex.
   For a function on {\rm R}$, quasiconvexity requires that each sublevel set be an interval (including, possibly, an inﬁnite interval). Convex functions have convex sublevel sets, and so are quasiconvex. But the converse is not true.
