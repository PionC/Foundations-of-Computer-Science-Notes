# **Set Theory**
## **Recap of Key Definitions**
### **Set Operations:**
[See 3. Sets and Formal Languages](3-Sets-and-Formal-Languages.md)
***
## **Set Equality**
Two sets are equal ($A=B$) if they contain the same elements
How to show equality?
* Examine all the elements
* Show $A\subseteq B$ and $B\subseteq A$
* Use the Laws of Set Operations

**Note that:** $A\backslash(B\backslash C)\neq (A\backslash B)\backslash C$
***
## **Laws of Set Operations**
For all sets $A$, $B$, $C$:
* **Commutativity:**
  * $A\cup B=B\cup A$
  * $A\cap B=B\cap A$
* **Associativity:**
  * $(A\cup B)\cup B=A\cup(B\cup C)$
  * $(A\cap B)\cap C=A\cap (B\cap C)$
* **Distribution:**
  * $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
  * $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$
* **Identity:**
  * $A\cup\emptyset=A$
  * $A\cap\mathcal{U}=A$
* **Complementation:**
  * $A\cup(A^c)=\mathcal{U}$
  * $A\cap(A^c)=\emptyset$
***
## **Derived Laws**
The following are all derivable from the previous 10 laws.
* **Idempotence:**
  * $A\cap A= A$
  * $A\cup A= A$
* **Double Complementation:**
  * $(A^c)^c=A$
* **Annihilation:**
  * $A\cap\emptyset=\emptyset$
  * $A\cup\mathcal{U}=\mathcal{U}$
* **De Morgan's Laws**
  * $(A\cap B)^c=A^c\cup B^c$
  * $(A\cup B)^c=A^c\cap B^c$
***
## **Two Useful Results**
**Duality**  
  **Definition:** If $A$ is a set defined using $\cap$, $\cup$, $\emptyset$ and $\mathcal{U}$, then $dual(A)$ is the expression obtained by replacing $\cap$ with $\cup$ (and vice-versa) and $\emptyset$ with $\mathcal{U}$ (and vice-versa).  
* **Theorem (Principle of Duality):**   
  If you can prove $A_1=A_2$ using the Laws of Set Operations then you can prove $dual(A_1)=dual(A_2)$.
* **Theorem (Uniqueness of Complement):**   
  $A\cap B=\emptyset$ and $A\cup B=\mathcal{U}$ if, and only if, $B=A^c$.
