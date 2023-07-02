# **Equivalence Relations and Partial Orders**
## **Equivalence Relations**
### **Definition:**
Equivalence relations capture a general notion of "equality".  
* **How to prove a Relation is a Equivalence Relation?**  
<u>A binary relation $R\subseteq S\times S$ is equivalence relation if it satisfies (R), (S), (T).</u>
  * **Reflexive (R):** Every object should <u>be "equal" to itself</u>.  
  $x=x$
  * **Symmetric (S):** if $x$ is "equal" to $y$, then $y$ should be "equal" to $x$.  
  $x=y \Rightarrow y=x$
  * **Transitive (T):** if $x$ is "equal" to $y$ and  $y$ is "equal" to $z$, then $x$ should be "equal" to $z$.  
  $x=y,\ y=z, \Rightarrow x=z$
### **Example:**  
Partition of $\mathbb{Z}$ into classes of numbers with the same remainder on division by $p$; it is particularly important for $p$ prime  
$\mathbb{Z}(p)=\mathbb{Z}_p={0, 1, ..., p-1}$   
One can define all four arithmetic operations (with the usual properties)on $\mathbb{Z}_p$ for a prime $p$; division has to be restricted when $p$ is not prime.
### **Rings:**
($\mathbb{Z}_p$, $+$, $\cdot$, 0, 1) are fundamental algebraic structures known as **rings**. These structures are very important in coding theory and cryptography. 
### **Equivalence Classes and Partitions**
Suppose $R\subseteq S\times S$ is an equivalence relation,  
The **equivalence class** $[s]$ (w.r.t. $R$) of an element $s\in S$ is   
$[s]=\{t:t\in S\ and\ sRt\}$  
**Fact:** $s$ $R$ $t$ if and only if $[s]=[t]$.  
![Equivalence-sRt](/6-img/equivalence-sRt.png)
### **Partitions:**
**Definition:**    
A **partition** of a set $S$ is a collection of sets $S_1, ..., S_k$ such that 
* $S_i$ and $S_j$ are disjoint(for $i\neq j$) -- no intersection
* $S=S_1\cup S_2\cup ...\cup S_k=\cup^k_{i=1}S_i$  

The collection of all equivalence classes $\{[s]:s\in S\}$ forms a partition of $S$.  
In the opposite direction, a partition of a set defines the equivalence relation on that set. If $S=S_1\cup S_2\cup ...\cup S_k$, then we can define $\sim\subseteq S\times S$ as:  
$s\sim t$ exactly when $s$ and $t$ belong to the same $S_i$.

***
## **Partial Oders**
### **Definition:**
A **partial order** $\preceq$ on $S$ <u>satisfies $(R)$, $(AS)$, $(T)$.</u>  
We call $(S, \preceq)$ a **poset** -- partially ordered set.
### **Examples of Poset:**
* Posets:
  * $(\mathbb{Z},\leq)$
  * $(POW(X),\subseteq)$ for some set $X$
  * $(\mathbb{N}, |)$
* Not posets:
  * $(\mathbb{Z},<)$
  * $(\mathbb{Z}, |)$
### **Hasse Diagram**
Every finite poset $(S, \preceq)$ can be represented with a **Hasse diagram**:  
* Nodes are elements of $S$
* An edge is drawn upward from $x$ to $y$ if $x\prec y$ and there is no $z$ such that $x\prec z\prec y$  
  **Example:** Hasse diagram for positive divisors of 24 ordered by $|$:  
  ![Hasse Diagram Example](/6-img/hasse-diagram-example.png)

### **Ordering Concepts**
**Minimal/Maximal/Minimum/Maximum:** 
Let $(S, \preceq)$ be a poset.
* **Minimal** element: $x$ such that there is no $y$ with $y\preceq x$ ------ **can be multiple minimal elements**  
  **Maximal** element: $x$ such that there is no $y$ with $x\preceq y$ ------ **can be multiple minimal elements**
* **Minimum(least)** element: $x$ such that $x\preceq y$ for all $y\in S$  
  **Maximum(greatest)** element: $x$ such that $y\preceq x$ for all $y\in S$
  * Minimum/Maximum elements are the **unique** minimal/maximal elements if they exist
  * Minimal/Maximum elements **always exist in finite posets**, but **not necessarily in infinite posets**.  

**Examples:**
* $POW(\{a, b, b\})$ with the order $\subseteq \emptyset$ is minimum; $\{a,b,c\}$ is maximum
* $POW(\{a, b, b\})\backslash \{\{a,b,c\}\}$ (proper subsets of $\{a,b,c\}$)  
  Each two-element subset $\{a,b\}$, $\{a,c\}$, $\{b,c\}$ is maximal.
    * But there is no maximum.  
  
![Order-Conpcept](/6-img/oder-concept.png)

**Upper Bound/ Lower Bound/...**
Let $(S, \preceq)$ be a poset.  
* $x$ is an **upper bound** for $A$ if $a\preceq x$ for all $a\in A$
* $x$ is an **lower bound** for $A$ if $x\preceq a$ for all $a\in A$
* The **set of upper bounds** for $A$ is defined as $ub(A)=\{x:a\preceq x\  for\ all\ a\in A\}$
* The **set of lower bounds** for $A$ is defined as $lb(A)=\{x:x\preceq a\  for\ all\ a\in A\}$
* The **least upper bound** of $A$, $lub(A)$, is the minimum of
$ub(A)$ (if it exists)
* The **greatest lower bound** of $A$, $glb(A)$, is the maximum of $lb(A)$ (if it exists)  

**glb and lub**  
To show $x$ is $glb(A)$ you need to show:  
* $x$ is a lower bound: $x\preceq a$ for all $a\in A$
* $x$ is the greatest of all lower bounds: If $y\preceq a$ for all $a\in A$.  

**Example:**  
$POW(X)$ ordered by $\subseteq$.
* $glb(A,B)=A\cap B$
* $lub(A,B)=A\cup B$ 

### **Lattice**
Let $(S, \preceq)$ be a poset.  
* $(S, \preceq)$ is a **lattice** if $lub(x,y)$ and $glb(x,y)$ exist for every pair of elements $x,y\in S$
* $(S, \preceq)$ is a **complete lattice** if $lub(A)$ and $glb(A)$ exist for every subset $A\subseteq S$.  

**Note that** 
* A finite lattice is always a complete lattice.  
  ![Lattice Examples](/6-img/lattice-example.png)
* An infinite lattice need not have a $lub$ (or no $glb$) for an arbitrary infinite subset of its elements, in particular no such bound may exist for all its elements.  
  ![Lattice Examples](/6-img/lattice-example2.png)


### **Total Orders**
A total order is a partial order that also satisfies:  
**Linearity (L)** (any two elements are comparable):  
For all $x,y$ either: $x<y$ or $y\leq x$(or both if $x=y$)
* On a finite set all total orders are "isomorphic"
* On an infinite set there is quite a variety of possibilities  
![Total Order Example](/6-img/total-order-example.png)

### **Ordering of a Poset -- Topological Sort**
For a poset $(S,\preceq)$ any total order $\leq$ that is consistent with $\preceq$ (if $a\preceq b$ then $a\leq b$) is called a **topological sort**.  
**Example:**  
![Topological Sort Example](/6-img/topological-sort-example.png)

### **Well-Ordered Sets**
A **well-ordered set** is a poset where every subset has a least element.
Notice that  
* The greatest element is not required.
* Well-ordered sets are an important mathematical tool to prove termination of programs.  
![Well-Odered Sets Example](/6-img/well-ordered-sets-example.png)

### **Orders for Cartesian Products and Languages**
There are several practical ways of combining orders:
* **Product Order:**   
  Given posets $(S,\preceq_S)$ and $(T,\preceq_T)$, define:  
  $(s,t)\preceq(s',t')$ if $s\preceq_S s'$ and $t\preceq_T t'$
* **Lexicographic Order:**  
  Given posets $(S,\preceq_S)$ and $(T,\preceq_T)$, define:  
  $(s,t)\preceq_{lex}(s',t')$ if $s\preceq_S s'$ or ($s=s'$ and $t\preceq_T t'$)  
  Extension to words: $\lambda \leq_{lex}w$ for all words
* **Lenlex Order:**  
  Lexicographic Ordering, but order by length first

**Note:**  
* No implicit weighting
* No bias toward any component
* In general, it is only a partial order, even if combining total orders
* No implicit weighting
