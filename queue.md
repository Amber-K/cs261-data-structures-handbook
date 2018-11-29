# Queue

A queue is a dynamic row of pieces of memory that all have their memory addresses in order. In a queue, the first variable put in must always be the first variable taken out.

# In Memory

In memory, a queue looks like this:

![Image of Queue in Memory](images/queue_memory.png)

\[description of diagram\]

# Operations

A queue supports the following operations:

* **Enqueue** is an O(1) constant time operation that puts a variable at the back end of a queue. The operation is constant time because there is always a stored pointer directing the computer straight to the back end of a queue.
* **Dequeue** also works in O(1) constant time, but it increments a front end pointer to remove a variable from the front end of the queue (the end opposite where data is enqueued); it then returns the removed variable. Dequeue is able to work in constant time thanks to the stored pointer that always points to the current front end of the queue.

# Use Cases

A queue is useful when data needs to be quickly piled up and the data that has been in the structure the longest needs to be the first data removed for use. The design of enqueue and dequeue naturally lends itself to processes using a first-in-first-out out model, and the O(1) constant time operation speeds of these operations make them especially attractive in such situations.

Queues are not useful when data needs to be accessed in any order other than first-in-first-out order. They do not have the operations that make it possible to access data other than whatever variable was enqueued first.

# Example

```
my_queue = queue()
my_queue.enqueue(1)
first_in_queue = my_queue.dequeue()
```

(c) 2018 Amber Kolar. All rights reserved.