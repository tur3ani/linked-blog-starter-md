it helps with finding the time complexity of [[algorithm]]

# how do we count the time complexity?
## example:
we have an array  | 3 | 2 | 4 | 5 | 8 |
	            0 1   2   3   4    
	with its size n = 5

----------------------------------------
``` C
Algorithm Sum(A,n) {
S = 0
for (i = 0; i < n; i++) {
s = s  + A[i];


}
return s;
}
```
with n being the array size and A being the array itself.
so lets find the Time complexity:
1- "S = 0" would equal *1 unit of time* since it is only initialized once.
2- the for loop  `for (i = 0; i < n; i++)`:
- the `i = 0` equals 1 unit of time.
- the `i < n` equals n + 1 units of time cause it repeats 5 times the size of the array then the sixth time which returns false and exit the loop.
- the `i++` equals n units of time cause it repeats after a successful loop.
- = all of this would be summed to be 2n + 2 which is the same as n + 1
3- `S = S + A[i]` would equal n units of time cause it is repeated with every for loop same as `i++`.
4- `return s` would equal 1 unit of time cause it is only repeated once.

the sum of all the previous would  give us: **f(n) = 2n + 3** 

# Space complexity:
taking the same example the space complexity would be:

1- the array size will be n the number of elements in it.
2- n , S , i all of them will have a space complexity of 1 unit.

Which will result in the space complexity of the algorithm being: **S(n) = n + 3**

