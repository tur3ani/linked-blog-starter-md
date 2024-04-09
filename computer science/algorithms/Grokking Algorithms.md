#algorithms #code #book #math #logic
# Definition
*An algorithm is a sequence of unambiguous instructions for solving a
problem, i.e., for obtaining a required output for any legitimate input in
a finite amount of time.*
# Table of Content

1- [[binary search]]

2- [[Running Time]]

3- [[Arrays and Linked lists]]

4- [[Selection sort]]

5- [[recursion]] 
###### RECAP
- Recursion is when a function calls itself.
- Every recursive function has two cases: the base case and the recursive case.
- A stack has two operations: push and pop.
- All function calls go onto the call stack.
- The call stack can get very large, which takes up a lot of memory.

6- [[Quicksort]]
###### RECAP
- D&C works by breaking a problem down into smaller and smaller pieces. If you’re using D&C on a list, the base case is probably an empty array or an array with one element.
- If you’re implementing quicksort, choose a random element as the pivot. The average runtime of quicksort is O(_n_ log _n_)!
- The constant in Big O notation can matter sometimes. That’s why quicksort is faster than merge sort.
- The constant almost never matters for simple search versus binary search, because O(log _n_) is so much faster than O(_n_) when your list gets big.
7- [[hash tables]] 

#### Recap

To recap, hashes are good for

- Modeling relationships from one thing to another thing
- Filtering out duplicates
- Caching/memorizing data instead of making your server do work.