#algorithms #code #list #logic 

# Difference
## Arrays
arrays size is initialized once it is not dynamic aka it cant changed higher or lower without changing its saving location this makes there is a work-around for this by making the array bigger than you initially wanted this though introduce a couple of problems mainly:

1- much wasted space if they end up left unused.
2- you might end up needing even more space so you will end up changing space location either way.
## Linked Lists
With linked lists, your items can be anywhere in memory, Each item stores the address of the next item in the list like “The next item can be found at address 123.” So you go to address 123, and it says, “The next item can be found at address 847,” and so on..  _AKA_ A bunch of random memory addresses are linked together, With linked lists, you never have to move your items. You also avoid another problem, the problem of arrays fixed size or not having enough space right next to each other to use like if i want to make a 10,000 sized array in my system i might have space for 10,000 but not side by side of each other but rather apart.

so why bother using *Arrays* if *Linked Lists* are that good?
well *Linked Lists* have a major problem of not being capable of jumping through the items 
since the address of the second item is saved with the first item and the save location of the third item is with the second item _etc._ 


### insertion to the middle of the list
_Linked Lists_ are better at insertion into the middle of it than _Arrays_ since in _Linked Lists_ it is as easy as changing the *space location* that is at the end of one of the elements
meanwhile in *arrays* you would need to change the entire *array* to do that 

### Deletions
again _Lists_ are better at this than _Arrays_ cause you just need to change what the previous element points to. With Arrays, everything needs to be moved up when you delete an element.

for deletions the [[Running Time]] would be O(n) for *Arrays* and O(1) for *Linked Lists*.
## Runtime


| X         | Arrays | Linked Lists |
| --------- | ------ | ------------ |
| Reading   | O(1)   | O(n)         |
| Insertion | O(n)   | O(1)         |
| Deletions | O(n)   | O(1)         |

O(n) = linear Time
O(1) = constant time

It’s worth mentioning that insertions and deletions are O(1) time only if you can instantly access the element to be deleted. It’s a common practice to keep track of the first and last items in a linked list, so it would take only O(1) time to delete those.