# Set

A set is a fixed row of pieces of memory that all have their memory addresses in order. Sets do not allow the variables stored within them to repeat. A set will often store a pointer of its first memory address that does not have a variable located at it. When a set's slots in memory are all in use and it needs room for more variables, it automatically makes a copy of itself twice as large in memory (with all its data stored in the first half of its new slots in memory), then deletes its original self.

# In Memory

In memory, a set looks like this:

![Image of Set in Memory](images/set_memory.JPG)

The rectangles represent pieces of memory. The pointer down below is keeping track of where the next available spot in the set is. It is important to remember that none of the values stored in this set are allowed to repeat.

# Operations

A set supports the following operations:

* **Access** returns a variable stored in the specified index (location in the set) in O(1) constant time. It always takes the same amount of time to access an element of a set because a set's first memory address is always stored and the following memory addresses are all in order. The index passed to the access function is multiplied by the size of the data type making up the set elements, then added to the base memory address. This tells the computer exactly where to look in memory to find the specified element of the set and always takes the same amount of computing.
* **Search** looks through every element to see if the specified variable value is stored in the set in O(n) linear time. For every variable added to a set, the search function must look through one more variable; the amount of time it takes to search a set increases linearly as new variables are added.
* **Insertion** puts a new variable into a specified location in a set, moving over any variables in the way; this happens in O(n) linear time. Having to move over all the variables that come after the point where one variable must be inserted causes the time insertions take to correlate directly with how many variables there are following the point of insertion.
* **Deletion** removes a variable at a specified location and moves all the following variables over to fill in the gap. This takes O(n) linear time because, like with insertions, the amount of time a deletion takes correlates directly with an arbitrary number of variables that have to move over.


# Use Cases

A set is useful when stored, non-repeating variables need to be accessed quickly because set access operations occur in constant time.

It is not useful when variables need to be searched for, inserted, or deleted quickly: all these operations occur in linear time.

# Example

```
my_set = {1, 2, 3, 4, 5}
accessed_variable = my_set[0]
variable_in_set = 4 in my_set
my_set.insert(2, 3)
del my_set[3]
```

(c) 2018 Amber Kolar. All rights reserved.