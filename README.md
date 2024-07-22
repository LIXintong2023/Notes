# Online optimization
## Definition
A field of optimization theory, more popular in computer science and operations research, that deals with optimization problems having no or incomplete knowledge of the future, opposed to the offline optimization problems where complete information is assumed.

In general, the output of an online algorithm is compared to the solution of a corresponding offline algorithm which is necessarily always optimal and knows the entire input in advance (competitive analysis).

Online optimization problems can be distinguished into online problems where multiple decisions are made sequentially based on a piece-by-piece input and those where a decision is made only once. 
## Famous problems
### Ski rental problem
A classical problem where a decision is made only once. 

It is currently a name given to a class of problems in which there is a choice between continuing to pay a repeating cost or paying a one-time cost which eliminates or reduces the repeating cost.

Consider a person who decides to go skiing, but for an undecided number of days. Renting skis costs $n$ per day, whereas buying a pair of skis costs $m$. If the person knows in advance how many days they want to ski, then the breakeven point is $m$ days. Fewer than $m$ days, renting is preferable, whereas with more than m days, buying is preferable. However, with no advance knowledge of how long one will be skiing, the breakeven point is unclear. A good algorithm will minimize the ratio of the cost when the number of days is known in advance to the cost when the number of days is not known in advance.

The best known deterministic algorithm for this problem is the break-even algorithm. This algorithm instructs one to rent for $(m-1)$ days and buy skis on the morning of day $m$ if one is still up for skiing. The worst-case for the break-even algorithm is that the person has to stop skiing after day $m$. In this case, her cost is $(n+m)$, which is $n/m$ more than that she would pay if she had known the number of days she would go skiing in advance. Thus, the competitive ratio for the break-even algorithm is $(n+m)/m$.
