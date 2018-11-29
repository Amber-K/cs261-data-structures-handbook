# Stack

A stack is a dynamic row of pieces of memory that all have their memory addresses in order. In a stack, the last variable put in must always be the first variable taken out.

# In Memory

In memory, a stack looks like this:

![Image of Stack in Memory](images/stack_memory.png)

\[description of diagram\]

# Operations

A stack supports the following operations:

* **Push** stores a variable at the top of a stack data structure in O(1) constant time. This operation always takes the same amount of time because a stack has a stored pointer that points straight to its top.
* **Pop** removes the variable at the top of a stack and returns it in O(1) constant time. The same pointer that makes constant time pushing possible tells pop which variable to remove; it works just as quickly for a pop as it does for a push.

# Use Cases

A stack is useful when data needs to be quickly piled up and the data most recently added to the structure needs to be the first data removed for use. The design of push and pop naturally lends itself to processes using a last-in-first-out out model, and the O(1) constant time operation speeds of these operations make them especially attractive in such situations.

Stacks are not useful when data needs to be accessed in any order other than last-in-first-out order. They do not have the operations that make it possible to access data other than whatever variable was pushed last.

# Example

```
my_stack = stack()
my_stack.push(1)
top_of_stack = my_stack.pop()
```

(c) 2018 Amber Kolar. All rights reserved.