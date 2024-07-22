# Online optimization
## Definition
A field of optimization theory, more popular in computer science and operations research, that deals with optimization problems having no or incomplete knowledge of the future, opposed to the offline optimization problems where complete information is assumed.

In general, the output of an online algorithm is compared to the solution of a corresponding offline algorithm which is necessarily always optimal and knows the entire input in advance (competitive analysis).

Online optimization problems can be distinguished into online problems where multiple decisions are made sequentially based on a piece-by-piece input and those where a decision is made only once. 

## Online algorithm
In computer science, an online algorithm is one that can process its input piece-by-piece in a serial fashion, i.e., in the order that the input is fed to the algorithm, without having the entire input available from the start. In contrast, an offline algorithm is given the whole problem data from the beginning and is required to output an answer which solves the problem at hand. 

## Competitive analysis
Competitive analysis is a method invented for analyzing online algorithms, in which the performance of an online algorithm is compared to the performance of an optimal offline algorithm that can view the sequence of requests in advance. An algorithm is competitive if its competitive ratio—the ratio between its performance and the offline algorithm's performance—is bounded. The ratio mentioned here referres to the ratio between the two (online and offline) algorithms when we encounter the worst case. In other words, the competitive ratio is calculated based on a situation where we use the resource at the most when employing the online algorithm.
Specifically, the competitive ratio of an algorithm, is defined as the worst-case ratio of its cost divided by the optimal cost, over all possible inputs. The competitive ratio of an online problem is the best competitive ratio achieved by an online algorithm. 

Intuitively, the competitive ratio of an algorithm gives a measure on the quality of solutions produced by this algorithm, while the competitive ratio of a problem shows the importance of knowing the future for this problem.
## Famous problems
### Ski rental problem
A classical problem where a decision is made only once. 

It is currently a name given to a class of problems in which there is a choice between continuing to pay a repeating cost or paying a one-time cost which eliminates or reduces the repeating cost.

Consider a person who decides to go skiing, but for an undecided number of days. Renting skis costs $n$ per day, whereas buying a pair of skis costs $m$. If the person knows in advance how many days they want to ski, then the breakeven point is $m$ days. Fewer than $m$ days, renting is preferable, whereas with more than m days, buying is preferable. However, with no advance knowledge of how long one will be skiing, the breakeven point is unclear. A good algorithm will minimize the ratio of the cost when the number of days is known in advance to the cost when the number of days is not known in advance.

The best known deterministic algorithm for this problem is the break-even algorithm. This algorithm instructs one to rent for $(m-1)$ days and buy skis on the morning of day $m$ if one is still up for skiing. The worst-case for the break-even algorithm is that the person has to stop skiing after day $m$. In this case, her cost is $(n+m)$, which is $n/m$ more than that she would pay if she had known the number of days she would go skiing in advance. Thus, the competitive ratio for the break-even algorithm is $(n+m)/m$.

### k-server problem
In this problem, an online algorithm must control the movement of a set of $k$ servers, represented as points in a metric space, and handle requests that are also in the form of points in the space. As each request arrives, the algorithm must determine which server to move to the requested point. The goal of the algorithm is to keep the total distance all servers move small, relative to the total distance the servers could have moved by an optimal adversary who knows in advance the entire sequence of requests. Up to 2014, reducing the competitive ratio to $k$ or providing an improved lower bound remains open.
