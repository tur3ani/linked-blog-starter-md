#algorithms #logic #programming 
>  [http://stackoverflow.com/a/72694/139117](http://stackoverflow.com/a/72694/139117) finding meaning in [[recursion]] 
> “Loops may achieve a performance gain for your program. Recursion may achieve a performance gain for your programmer. Choose which is more important in your situation!”
> 


recursion (العودية أو التكرار) means: **defining a problem in terms of itself**
it is a messed up way to write programs that most of the time doesn't increase productivity but rather your headache, but hey at least it looks cool and big-brained way to do things

## Base case and recursive case
because a recursive case calls itself it is easy to fall into an infinite loop.
this is why there is a recursive case and a base case for recursive functions.
the recursive case here is the part we want to call recursively,
while the base case will be the return statement that exits the function to not fall to a infinite loop.
most common way to achieve a _Base case_ and _recursive case_ will be an *if statement*.

## The stack

