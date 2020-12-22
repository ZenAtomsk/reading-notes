# Stacks and Queues

## What is a Stack

a stack of boxes

data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Common terminology:

- **Peek O(1)** - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
- **IsEmpty O(1)** - returns true when stack is empty otherwise returns false.
- **Push O(n)** - Nodes or items that are put into the stack are pushed
- **Top** - This is the top of the stack.
- **Pop O(1)** - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

**First In Last Out**

Exceptions raised when node is empty.

## What is a Queue

a line of people

- **Peek** - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
- **plIsEmpty** - returns true when queue is empty otherwise returns false.
- **Front** - This is the front/first Node of the queue.
- **Dequeue** - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
- **Rear** - This is the rear/last Node of the queue.
- **Enqueue O(1)** - Nodes or items that are added to the queue.

**First In First Out**