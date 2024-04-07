# Big O notation
## growth rate:
[[algorithm]] have different growth rate than each other, _what do we mean by that?_
lets take a search algorithm for a rocket landing location on the moon on one hand so if we take a list of 100 element as an example test and lets assume checking each element takes 1ms and we have a *10 seconds* time limit that we don't want to go above:
[[binary search]] will solve it faster at around 7 ms meanwhile simple search will take 100ms 
that means that [[binary search]] is around 15 times faster than simple search, so if we test case a list of 1 million elements, [[binary search]] will take around 30 ms, and since [[binary search]] is around 15 times more efficient then simple search will be :$$ 15 * 30 = 450ms $$
that is still way under the 10 seconds limit so we can just simply use simple search instead of [[binary search]] to avoid bugs, _right_?

No. Turns out, this is dead wrong. The run time for simple search with 1 billion items will be 1 billion ms, which is 11 days! The problem is, the run times for binary search and simple search _don’t grow at the same rate_.
now cause of this problem:
> Big O notation tells you how fast an algorithm is. For example, suppose you have a list of size _n_. Simple search needs to check each element, so it will take _n_ operations. The run time in Big O notation is O(_n_). Where are the seconds? There are none—Big O doesn’t tell you the speed in seconds. _Big O notation lets you compare the number of operations._ It tells you how fast the algorithm grows.

so the BIG O is from Operations 