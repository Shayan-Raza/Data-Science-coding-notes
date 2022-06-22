# Big O Notation
Big O Notation is a way to quickly write what the complexity of an algorithm is

---
*From fastest to slowest*
## Logarithmic time
**O(log(n))**
Runtime goes slower than the input size

***Example***: Binary Search 

## Linear time
**O(n)**
Runtime grows at the same rate as input 

***Example***: Unsorted list search

## Log-Linear time
**O(n log(n))**
An operation of log(n) complexity for each input value

***Example***: Efficient Sorting

## Quadratic time
**O(n2)**
An operation of complexity O(n) is carried out for each input

***Example***: Check for all pairs of input Values

## Polynomial time
**O(n^3<)**
Computations with other exponents

***Example***: Check all triplets of input values

## Exponential time
**O(2^n)**
Complexity is multiplied with each additional input value

***Example***: Recursive Algorithms

## Factorial time
**O(n!)**
Runtime can be worse than exponential

***Example***: ![[Counting#Permutations]]