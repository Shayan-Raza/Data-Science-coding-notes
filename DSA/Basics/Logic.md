# Logic 
---
## Operators 
> Variables and operators are used to model numerical problems. The result is not in numbers but instead in True / False

***Expressing Dependencies***
Dependencies are expressed with the -> operator. A -> B is the idea that if A is True then B will also be True

***Negating Ideas***
To negate ideas we use ! **Negation operator** meaning opposite ex: !A means the opposite on A

***The Bi-conditional***
Be careful, saying “if the pool is warm, I’ll swim”
doesn’t mean I’ll only swim in warm water. The statement promises
nothing about cold pools. In other words, A → B doesn’t mean
B → A. To express both conditionals, use the bi-conditional:
A ↔ B : I’ll swim if and only if the pool is warm.
Here, the pool being warm is equivalent to me swimming: knowing
about the pool means knowing if I’ll swim and vice-versa. 

***And, Or, Exclusive Or***
*And* = All ideas are True
*Or* = Any idea is True 
*Exclusive Or* = XOR = Ideas are of opposing truths 

![[Pasted image 20220525214712.png]]
*Credit: Computer Science Distilled*

## Boolean Algebra
As elementary algebra simplifies numerical expressions, boolean
algebra simplifies logical expressions.

***Associativity***
Parentheses are irrelevant for sequences of AND or
OR operations. As sequences of sums or multiplications in elementary algebra, they can be calculated in any order.

***Distributivity***
ANDing after an OR is equal to ORing the results of the ANDs and vice versa. 
> A AND (B OR C) = (A AND B) OR (A AND C).
> A OR (B AND C) = (A OR B) AND (A OR C).

***Logic gates***
Logic gates perform logic operations on electric
current. Logic gates receive values through input wires performs its operation and places the result on its output wire. The types of gates are: 
- AND gates 
- OR gates 
- XOR gates 


