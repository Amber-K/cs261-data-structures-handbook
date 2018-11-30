# Priority Queue

A priority queue is made from a min or max heap. Min and max heaps binary heaps made using dynamic arrays in memory. A priority queue has variables enqueued and dequeued, but the variable dequeued is always the variable with the highest priority. The highest priority variable will be the smallest variable in the priority queue if it is using a min heap; the largest variable if the priority queue uses a max heap.

# In Memory

In memory, a priority queue looks like this:

![Image of Priority Queue in Memory](images/priority_queue_memory.png)

\[description of diagram\]

# Operations

A priority queue supports the following operations:

* **Enqueue** a piece of data is added to the array that makes up the min/max heap in a place that situates this data in the first open space at the bottom of the min/max heap when viewing its nodes from left to right. This always happens in O(1) constant time because it takes a single calculation to find the next open place in the array. However, it then takes O(log(n)) logarithmic time for the inserted data point to bubble up as high as it needs to go in the min/max heap because the data point must be compared to a piece of data on each of the min/max heap's levels until the new data reaches its correct location. It stops when it is larger than its parent data point (in the case of a min heap) or when it is smaller than its parent data point (in the case of max heap). 
* **Dequeue** always removes the root data point and returns its value when a min/max heap is being used as a priority queue. However, before it stops, the operation must compare the old root's children to pick the new root—which will either be the smallest or the largest, depending on whether this is a min or a max heap. Once the operation has picked a direction, it will then push its way down recursively, forcing higher priority data points up to fill in the newly-created gap at the top of the structure. Similarly to enqueues, this would be an O(1) constant time operation if all that had to happen was the actual removal and returning of the root. However, the additional mechanics make dequeues O(log(n)) logarithmic time operations as well, since they must push down through all the levels of a balanced tree until they reach leaves.

# Use Cases

A priority queue is useful when the most significant data stored in a data structure needs to be the first data removed for use. Priority queue operations are designed to quickly handle priority-based situations like these.

Because they have a limited selection of operations, priority queues can not handle situations other than the specific, priority-based enqueuing and dequeuing situations they are designed to excel at.

# Example

```
my_priority_queue = priority_queue()
my_priority_queue.enqueue(1)
dequeued_value = my_priority_queue.dequeue()
```

(c) 2018 Amber Kolar. All rights reserved.