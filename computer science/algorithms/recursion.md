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
inn [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), a **stack** is an [abstract data type](https://en.wikipedia.org/wiki/Abstract_data_type "Abstract data type") that serves as a [collection](https://en.wikipedia.org/wiki/Collection_(abstract_data_type) "Collection (abstract data type)") of elements with two main operations:

- **Push**, which adds an element to the collection, and
- **Pop**, which removes the most recently added element.

### Call stack 
a **call stack** is a [stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type) "Stack (abstract data type)") data structure that stores information about the active [subroutines](https://en.wikipedia.org/wiki/Subroutine "Subroutine") of a [computer program](https://en.wikipedia.org/wiki/Computer_program "Computer program"). This type of stack is also known as an **execution stack**, **program stack**, **control stack**, **run-time stack**, or **machine stack**, and is often shortened to simply "**the stack**". Although maintenance of the call stack is important for the proper functioning of most [software](https://en.wikipedia.org/wiki/Software "Software"), the details are normally hidden and automatic in [high-level programming languages](https://en.wikipedia.org/wiki/High-level_programming_language "High-level programming language"). Many computer [instruction sets](https://en.wikipedia.org/wiki/Instruction_set "Instruction set") provide special instructions for manipulating stacks.

 _when you call a function from another function, the calling function is paused in a partially completed state._ All the values of the variables for that function are still stored in memory.

Using the stack is convenient, but there’s a cost: saving all that info can take up a lot of memory. Each of those function calls takes up some memory, and when your stack is too tall, that means your computer is saving information for many function calls. At that point, you have two options:

- You can rewrite your code to use a loop instead.
- You can use something called _tail recursion_. That’s an advanced recursion topic that is out of the scope of this book. It’s also only supported by some languages, not all.




> [!to my future self] Title
> go through and read on tail recursion .


