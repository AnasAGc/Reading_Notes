# Stacks and Queues

## Stacks:

 Stack is collection of elements, that follows the LIFO order. LIFO stands for Last In First Out, which means element which is inserted most recently will be removed first. Imagine a stack of tray on the table. When you put a tray there you put it at top, and when you remove it, you also remove it from top.

A stack has a restriction that insertion and deletion of element can only be done from only one end of stack and we call that position as top. The element at top position is called top element. Insertion of element is called PUSH and deletion is called POP.


A stack is a container of objects that are inserted and removed according to the last-in first-out (LIFO) principle. In the pushdown stacks only two operations are allowed: push the item into the stack, and pop the item out of the stack. A stack is a limited access data structure - elements can be added and removed from the stack only at the top. push adds an item to the top of the stack, pop removes the item from the top. A helpful analogy is to think of a stack of books; you can remove only the top book, also you can add a new book on the top.

A stack is a recursive data structure. Here is a structural definition of a Stack:

* a stack is either empty or
* it consistes of a top and the rest which is a stack;

### Applications

* The simplest application of a stack is to reverse a word. You push a given word to stack - letter by letter and then pop letters from the stack.

* Another application is an "undo" mechanism in text editors; this operation is accomplished by keeping all text changes in a stack.

## Queue:

Queue is a data structure that follows the FIFO principle. FIFO means First In First Out i.e the element added first in the queue will be the one to be removed first. Elements are always added to the back and removed from the front. Think of it as a line of people waiting for a bus at the bus stand. The person who will come first will be the first one to enter the bus.

The circular queue implementation is done by using the modulo operator (denoted %), which is computed by taking the remainder of division (for example, 8%5 is 3). By using the modulo operator, we can view the queue as a circular array, where the "wrapped around" can be simulated as "back % array_size". In addition to the back and front indexes, we maintain another index: cur - for counting the number of elements in a queue. Having this index simplifies a logic of implementation.

### Applications

The simplest two search techniques are known as Depth-First Search(DFS) and Breadth-First Search (BFS). These two searches are described by looking at how the search tree (representing all the possible paths from the start) will be traversed.