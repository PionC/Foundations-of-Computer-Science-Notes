# **Introduction**
## **Four main topics of Computer Science in this repo:**
* **Structures**
  * Set Theory
  * Formal Languages
  * Relations
  * Functions
  * Graph Theory
* **Recursion**
  * Recursion
  * Algorithmic Analysis
  * Induction
* **Logic**
  * Boolean Logic
  * Propositional Logic
* **Probability**
  * Combinatorics
  * Probability
  * Statistics
  
## **Proposition Structure:**
* If $A$ then $B$ ($A \Rightarrow B$)
* $A$ if and only if $B$ ($A\Leftrightarrow B$)
* For all $x$, $A$ ($\forall x. A$)
* There exists $x$ such that $A$ ($\exists x.A$)
  
## **Negating Propositions:**
| Proposition Form | Negation |
| :---------------:| :------:|
| $A$ and $B$ | not $A$ or not $B$ |
| $A$ or $B$ | not $A$ and not $B$ |
| $A \Rightarrow B$ | $A$ and not $B$ |
| $A \Leftrightarrow B$ | $A$ and not $B$, or $B$ and not $A$ |
| $\forall x.A$ | $\exists x. not A$ |
| $\exists x.A$ | $\forall x. not A$ |

## **Proof Strategies:**
* Direct proof
* Contradiction: Using negation propositions
* Contrapositive:
  * To prove "If $A$ then $B$", you can prove "If not $B$ then not $A$"
* Dealing with $\forall$: In order to check infinitely many cases, we can:
  * Choose an arbitrary element: an object with no assumptions about it (may have to check several cases)
  * Induction 
