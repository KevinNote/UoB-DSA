# Queue/队列

FIFOs, First-In-First-Out#

## ADT

- `enqueue(x)`
- `dequeue`
- `is_empty()`

![](img/q-0.png)

If try to dequeue from an empty queue, will get `EmptyQueueException`.

## Implementation

### By Array

Whenever `enqueue` (resp. `dequeue`) we increment `rear` (resp. `front`).

![](img/q-i0.png)

#### Representing circles

![](img/rep-cir.png)

```
pos = (pos + 1) % 6
```

To generalise:

```
pos = (pos + 1) % size
```

#### Circular Queue

```csharp
var queue = new int[MAXQUEUE];
int front = 0;
int size = 0;
```

- `font + size <= MAXQUEUE`  
`pos` ∈ [font, font + size)  
![](img/cq-0.png)
- `font + size > MAXQUEUE`  
`pos` ∈ [font, MAXQUEUE) ∪ [0, front + size - MAXQUEUE)
![](img/cq-1.png)

- `font` ∈ [0, MAXQUEUE)
- `size` ∈ [0, MAXQUEUE]

`rear = (front + size) % MAXQUEUE`

if `size == MAXQUEUE`, the queue is full.

##### Enqueue

1. Is not full?
2. Insert data into index `(front + size) % MAXQUEUE`
3. Add 1 to `size`

##### Dequeue

1. Is not empty?
2. Get value at index `front`
3. `front = (front + 1) % MAXQUEUE`
4. Minus 1 to `size`