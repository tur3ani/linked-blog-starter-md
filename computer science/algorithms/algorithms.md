#code #algorithms #math 


# Definition:
what is algorithms?: *it is a step by step to solve a problem*
what is a program?: *it is a step by step to solve a problem*
so what is the difference between them?
## difference between algorithms and programs

| X            | Algorithm        | Program              |
| ------------ | ---------------- | -------------------- |
| usage        | Design           | Implementation       |
| writer       | Domain knowledge | Programmer           |
| language     | any language     | programming language |
| dependencies | Hardware / OS    | Hardware / OS        |
| purpose      | Analyze          | Testing              |
# Characteristics of Algorithms
1. it can take 0 or more input
2. it must generate at least one output
3. definiteness --> every value must be clear and a human can solve it EX: you cant use (-1^1/2) 
4. Finiteness: it must never have an infinite loop in it this is a must for point 2 since you cant output anything if you never exit the loop.
5. Effectiveness: you mustn't use or do anything that doesnt have to do with the item and purpose at hand.

# How to Analyze an Algorithm
1. Time: it is a time Function
2. space
3. data transfer (N / W)
4. power
5. CPU Registers
## so how do we find the time or space time?
time :every statement -simple statement- take one unit of time so here 
```
Algorithm Swap(a,b)
 temp = a;
 a = b;
 b = temp;

```
this algorithm takes 3 units of time -f(n) = 3- cause it has 3 simple statements
x = 5 * a + 6 * 5 in algorithm this takes one unit of time but in code it might take more
space: is based on how many variables is used so it is constant O(n)

