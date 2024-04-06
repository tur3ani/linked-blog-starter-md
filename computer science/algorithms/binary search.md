#algorithms #logic #math #programming

# how it works
it works by searching a *sorted list* from half of it and identifying if it went too high or low then going through the lower or higher half again depending on the former answer making it take only :

$time complexity = log_2n$
with n being the size of the list 
making it much more efficient than simple search by going over all the elements of the list until a match is found

## python example:
The binary search function takes a sorted array and an item. If the item is in the array, the function returns its position. You’ll keep track of what part of the array you have to search through. At the beginning, this is the entire array:

``` python
low = 0
high = len(list) - 1

```


Each time, you check the middle element:
```python
mid = (low + high) / 2
guess = list[mid]
```

If the guess is too low, you update low accordingly:

``` python
if guess < item:
  low = mid + 1
```

And if the guess is too high, you update high.
### EXERCISES
> **1.1**
> 
> Suppose you have a sorted list of 128 names, and you’re searching through it using binary search. What’s the maximum number of steps it would take?
$$ log_2128  = 7$$
1.2 Suppose you double the size of the list. What’s the maximum number of steps now?
$$ log_2256 = 8 $$

## [[Running Time]]
its running time is logarithmic time (or log time, as the natives call it), so time complexity will be
$$ O(log_2n) $$
so for example if we have a list of 100 items a simple search will at most need 100 units of time 
meanwhile binary search will need at most :$$ log_2100 = 7 $$
 If it’s a list of 4 billion numbers, it takes up to 4 billion guesses. So the maximum number of guesses is the same as the size of the list. This is called _linear time_( O(n)).
 meanwhile binary search will take at most $$ log_24billions = 32 $$
 32 guesses powerful, eh?
