# **Relations**
## **Intro**
### **Relations**
Relations are an abstraction used to <u>capture the idea that the objects from certain domains </u>(often the same domain for several objects) are related. These objects my
* influence one another (each other for binary relations; self(?) for unary)
* share some common properties
* correspond to each other precisely when some constraints are satisfied

### **Functions**
Functions capture the idea of transforming inputs into outputs.
***
## **Definition**
An **n-ary relation** is a subset of the cartesian product of n sets.  
$R\subseteq S_1\times S_2\times...\times S_n$  
To show tuples related by $R$ we write:  
$(\times_1, \times_2, ..., \times_n)\in R$ or $R(\times_1, \times_2, ..., \times_n)$  
<u>If $n=2$, we have a **binary** relation $R\subseteq S\times T$ and to show pairs related by R we write:  
$(x, y)\in R$ or $R(x, y)$ or $\times Ry$</u>  
**Note:** $(x, y)\in R$ means $x$ is related to $y$ on relation $R$.  
Universe: $\mathcal{U}=S_1\times S_2\times ...\times S_n$ in the **domain** of $R$, and we say $R$ is a relation on $\mathcal{U}$ (or **on** $S$ if $S_1=...=S_n=S$ and $n$ is clear).  
**E.g.** $R$ is a binary relation **on** $S$ $\Leftrightarrow$ $R\subseteq S\times S$   
**Defining Relations:**  
Just as with sets $R$ can be defined by
* explicit enumeration of interrelated k-tuples (ordered pairs in case of binary relations);  
* properties that identify relevant tuples within the entire $S_1\times S_2\times...\times S_k$  
* construction from other relations (e.g. union, intersection,
complement etc).

***
## **Binary Relations**
**Definition:**  
A **binary relatioin** between $S$ and $T$ is a subset of $S\times T$: i.e. a set of ordered pairs.  
Also: over $S$ and $T$; from $S$ to $T$; on $S$ (if $S=T$).  
**Defining Binary Relations: Matrix Representation**  
Defining a relation $R\subseteq S\times T$:
Rows enumerated by elements of $S$, columns by elements of $T$.
**Defining Binary Relations: Graph Representation**  
If $S=T$ we can define $R\subseteq S\times S$ as a directed graph: represent elements of $S$ as Nodes, and elements of $R$ as Edges.
### **Operations for binary relations**
Relations are sets, so the standard set operations ($\cap$, $\cup$, $\backslash$, $\oplus$, etc) can be used to build new relations.  
Two operations that apply to binary relations uniquely:
* **Converse:**  
  If $R\subseteq S\times T$ is a relation, then $R^{\leftarrow}\subseteq T\times S$:  
  $R^{\leftarrow}\overset{\operatorname{def}}{=}\set{(t,s)\in T\times S:(s,t)\in R}$
  * **Fact:** $(R^\leftarrow)^\leftarrow=R$
* **Composition:**  
  If $R_1\subseteq S\times T$ and $R_2\subseteq T\times U$, then $R_1;R_2\subseteq S\times U$:  
  $R_1;R_2\overset{\operatorname{def}}{=}\set{(s,u)\in S\times U:\ there\ exists\ t\in T\ such\ that\ (s,t)\in R_1\ and\ (t,u)\in R_2}$   
![Converse-1](/5-img/converse1.png)
![Converse-2](/5-img/converse2.png)
### **Relational Images**
Given $R\subseteq S\times T,\ A\subseteq S,\ and\ B\subseteq T$.
**Definition:**  
* Relational Image of $A$, $R(A)$:  
  $R(A)\overset{\operatorname{def}}{=}\set{t\in T :\ (s,t)\in R\ for\ some\ s\in A}$
* Relational pre-image of $B$, $R^\leftarrow(B)$:  
  $R^\leftarrow(B)\overset{\operatorname{def}}{=}\set{s\in S:\ (s,t)\in R\ for\ some\ t\in B}$.  
![Relational Image-1](/5-img/relational-image1.png)
![Relational Image-2](/5-img/relational-image2.png)
![Relational Image-3](/5-img/relational-image3.png)
![Relational Image-4](/5-img/relational-image4.png)
![Relational Image-5](/5-img/relational-image5.png)
***
## **Properties of Binary Relations**
A binary relation $R\subseteq S\times T$ is:
* **Functional:** (Fun)   
  For all $s\in S$ there is <u>at most</u> one $t\in T$ such that $(s,t)\in R$  
* **Total:** (Tot)   
  For all $s\in S$ there is <u>at least</u> one $t\in T$ such that $(s,t)\in R$  
* **Injective:** (Inj) [See more details](https://en.wikipedia.org/wiki/Injective_function)   
  For all $t\in T$ there is <u>at most</u> one $s\in S$ such that $(s,t)\in R$  
* **Surjective** (Sur)  [See more details](https://en.wikipedia.org/wiki/Surjective_function)  
  For all $t\in T$ there is <u>at least</u> one $s\in S$ such that $(s,t)\in R$  
* **Bijective** (Bij) [See more details](https://en.wikipedia.org/wiki/Bijection)  
  Injective and Surjective.
### **Functions and Function Properties**
* **Partial Function** is a binary relation that is (Fun).
* A **Function** is a binary relation that is (Fun) and (Tot).
* An **Injection** is a function that is (Inj). (Injection or 1-1 one-to-one)
* A **Surjection** is a function that is (Sur). (or called onto $lm(f) = Codom(f)$)
* A **Bijection** is a function that is (Bij).
![Function](/5-img/function.png)  
![Function](/5-img/injection.png)  
![Function](/5-img/surjection.png)  
#### **Properties of Binary Relations $R\subseteq S\times S$**
* **Reflexive** (R):  
  For all $x\in S$: $(x,x)\in R$
  Everything is related to itself.  
  **E.g.** equal to ($=$)  
  ![Reflexive](/5-img/reflexivity.png)
* **Antireflexive** (AR):
  For all $x\in S$: $(x,x)\notin R$
  Nothing is related to itself.  
  **E.g.** less than ($<$), or not equal to ($\neq$).  
  ![Antireflexive](/5-img/antireflexivity.png)
* **Symmetric** (S):
  For all $x,y\in S$: if $(x,y)\in R$, then $(y,x)\in R$  
  If $x$ is related to $y$, then $y$ is related to $x$. The direction doesn't matter.  
  **E.g.** if $x=y$, then $y=x$.  
  **Note: Non-symmetric** -- $x$ is related to $y$, but $y$ is NOT related to $x$.  
  ![Antireflexive](/5-img/symmetric.png)
* **Antisymmetric** (AS):
  For all $x,y\in S$: if $(x,y)\in R$ and $(y,x)\in R$, then $x=y$  
  If $x$ is related to $y$ and $y$ is related to $x$, then $x=y$.  
  ![Antisymmetric](/5-img/antisymmetry.png)
* **Transitive** (T):  
  For all $x,y,z\in S$: if $(x,y)\in R$ and $(y,z)\in R$, then $(x,z)\in R$  
  If $x$ is related to $y$ and $y$ is related to $z$, then $x$ is related to $z$.  
  ![Antisymmetric](/5-img/transitivity.png)

**Note**:
* Properties have to hold for all elements
* (S), (AS), (T) are conditional statement - they will still hold even if there is nothing which satisfies the 'if' part  
* When the domain is emptyset, all of these conditions are true for the empty relation.  
### **Interaction of Properties**
A relation <u>**can be** both symmetric and antisymmetric.</u> Namely, when $R$ consists only of some pairs $(x,x),x\in S$.  
A relation <u>**can not be** simultaneously reflexive and antireflexive.</u> (unless $S=\emptyset$).  
**Note:** nonreflexive $\nLeftrightarrow$ antireflexive/irreflexive, nonsymmetric $\nLeftrightarrow$ antisymmetric
***
## **Functions**
### **Definition**
A function, $f:S\rightarrow T$, is a binary relation $f\subseteq S\times T$ that satisfies (Fun) and (Tot). That is, <u>**for all**</u> $s\in S$ there is <u>**exactly one**</u> $t\in T$ such that $(s,t)\in f$.  
**Note:** We denote the unique element related to $s$ as $f(s)$ and the set of all functions from $S$ to $T$ as $T^S$.  
**Explaination:** $f:S\rightarrow T$ describes pairing of the sets: it means that $f$ assigns to every element $s\in S$ a <u>unique</u> element $t\in T$. <u>To emphasise where a specific element is sent, we can write $f:x\rightarrowtail y$, which means the same as $f(x)=y$.</u>  
**Important:** The domain and co-domain are critical aspects of a function's definition.  
$f:\mathbb{N}\rightarrow\mathbb{Z}$ given by $f(x)\rightarrowtail x^2$ and $g:\mathbb{N}\rightarrow\mathbb{N}$ given by $g(x)\rightarrowtail x^2$ are different functions even though they have the same behaviour.   
![Symbol](/5-img/symbol.png)  
![Function-example](/5-img/function-example.png)  

### **Converse of A Function**
Question: $f^\leftarrow$ is relation; when is it a function?

### **Functions on Finite Sets**  
For a **finite** set **S** and $f:S \rightarrow S$ the properties.
* surjective, and
* injective  

are equivalent.

