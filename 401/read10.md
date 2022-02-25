# Stacks and Queues

## Read 10

### Joshua McCluskey

### What is a stack

- Stacks are a LIFO construction Last In First Out or FILO Fisrt in last Out conssisting of nodes
- Like a stack of plates, the last plate on the stack will be used.
- With a stack you `push pop peek`
- When you `push` you add it an O (1) time It take sthe same amount of time no matter how many nodes
- `top` is at the top of the stack if you want to move top use `top next`
- `pop ` removes the top from the stack and reassigns top to the next node
- Check if empty before popping
- Have a temp node that points to the same node at the top reassign the next value to the top
- temp node is the popped node
- `peek` - top.value
- `isEmpty` - top = null


### What is a Queue

- Queues are a data structure FIFO First in First out or LILO Last in Last out data structure
- Like a lin at the grocery store you wait, and the front person is being helped and the line continues to get longer from the rear
- `enqueue` adds a node to the rear of the queue it is an O (1 ) operation is the same no matter how many nodes
- With the Queue we are reassigning the rear 
- `dequque` removes the nodes from the front of the queue
- you would use a temp node for the dequeue node and reassign the front node.
- `peek` front.value
- `isEmpty` front = null



[<=== Back](../README.md)