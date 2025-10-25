 $\mathcal{O}(n!)$ or **Factorial Time** complexity represents the absolute worst-case scenario for efficiency and is the fastest-growing complexity rate after exponential time, $\mathcal{O}(2^n)$. These algorithms are entirely impractical for all but the smallest inputs.

![](https://github.com/TechCraft-By-Subrata/JavaScript-DSA/blob/main/images/travelling_salesperson.jpg)
***

## Real-World $\mathcal{O}(n!)$ Example: The Traveling Salesperson Problem (Brute-Force) 🏙️

The classic, real-world example of $\mathcal{O}(n!)$ complexity is finding the most efficient route for a **Traveling Salesperson** using a **brute-force** approach.

Imagine a salesperson who needs to visit a list of $n$ cities and return home, minimizing the total travel distance. To guarantee finding the shortest route, the brute-force approach requires checking **every single possible sequence** (permutation) of cities.

| Characteristic | Mapping to Big O |
| :--- | :--- |
| **Number of Cities to Visit** | Represents the input size, $n$. |
| **Checking All Possible Routes** | Represents the time complexity, $\mathcal{O}(n!)$. |

### The Process: Factorial Growth

The number of unique paths to check grows factorially:

1.  **1 City ($n=1$):** (Start $\rightarrow$ City 1 $\rightarrow$ Start).
    * Routes: $1! = 1$
2.  **2 Cities ($n=2$):** (Start $\rightarrow$ C1 $\rightarrow$ C2 $\rightarrow$ Start) and (Start $\rightarrow$ C2 $\rightarrow$ C1 $\rightarrow$ Start).
    * Routes: $2! = 2$
3.  **3 Cities ($n=3$):**
    * For the first city, you have 3 choices.
    * For the second city, you have 2 remaining choices.
    * For the third city, you have 1 remaining choice.
    * Routes: $3 \times 2 \times 1 = 3! = 6$
4.  **$n$ Cities:**
    * Routes: $n \times (n-1) \times (n-2) \times \dots \times 1 = n!$

### The Factorial Breakdown

The effect of factorial growth is immediate and catastrophic:

| Number of Cities ($n$) | Total Routes ($n!$) | Real-World Effort (If 1 check = 1 second) |
| :---: | :---: | :--- |
| **5** | 120 | 2 minutes |
| **10** | $3.6$ million | $\approx 42$ days |
| **15** | $1.3$ trillion | $\approx 41,000$ years |
| **20** | $2.4 \times 10^{18}$ | **77 billion years** |

Adding just one city, moving from $n=15$ to $n=16$, means multiplying the effort by **16 times**. This growth rate is so extreme that $\mathcal{O}(n!)$ algorithms are rarely used for problems with $n$ greater than about 10 to 12. For larger problems, computer scientists must use heuristic algorithms that find *good* solutions, even if they can't mathematically guarantee the *best* solution. 
