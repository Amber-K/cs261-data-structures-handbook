# Tuple

A tuple is a fixed row of pieces of memory that all have their memory addresses in order. Tuples are immutable, which means that once one is initialized, its contents will not be able to be changed.

# In Memory

In memory, a tuple looks like this:

![Image of Tuple in Memory](images/tuple_memory.png)

\[description of diagram\]

# Operations

A tuple supports the following operations:

* **Access** returns a variable stored in the specified index (location in the tuple) in O(1) constant time. It always takes the same amount of time to access an element of a tuple because a tuple's first memory address is always stored and the following memory addresses are all in order. The index passed to the access function is multiplied by the size of the data type making up the tuple elements, then added to the base memory address. This tells the computer exactly where to look in memory to find the specified element of the tuple and always takes the same amount of computing.
* **Search** looks through every element to see if the specified variable value is stored in the tuple in O(n) linear time. For every variable added to a tuple, the search function must look through one more variable; the amount of time it takes to search a tuple increases linearly as new variables are added.

# Use Cases

A tuple is useful when constant variables need to be accessed quickly because tuple access operations occur in constant time.

It is not useful when variables need to be searched for, inserted, or deleted: searching occurs in O(n) linear time and there can not be insertions or deletions.

# Example

```
my_tuple = (1, 2, 3, 4, 5)
accessed_variable = my_tuple[0]
variable_in_tuple = 2 in my_tuple
```

(c) 2018 Amber Kolar. All rights reserved.