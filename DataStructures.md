At a high level, there are basically three types of data structures. 
- `Stacks` and `Queues` are array-like structures that differ only in how items are inserted and removed. 
- `Linked Lists`, `Trees`, and `Graphs` are structures with nodes that keep references to other nodes. 
- `Hash Tables` depend on hash functions to save and locate data.

In terms of complexity, 
- Stacks and Queues are the simplest and can be constructed from Linked Lists. 
- Trees and Graphs are the most complex because they extend the concept of a linked list. 
- Hash Tables need to utilize these data structures to perform reliably. 

In terms of efficiency, 
- Linked Lists are most optimal for recording and storing of data, 
- Hash Tables are most performant for searching and retrieving of data.


![Stack & Queue](https://res.cloudinary.com/practicaldev/image/fetch/s--BgQwtlaT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/1600/1%2AxSRTv4g2tofWQktkUwoRog.png)

## Stack


Arguably the most important Stack in JavaScript is the `call stack` where we push in the scope of a function whenever we execute it.

Programmatically, it’s just an `array` with two principled operations: `push` and `pop`. 

`Push` adds elements to the top of the array, while `Pop` removes them from the same location. 

In other words, Stacks follow the “Last In, First Out” protocol (LIFO).


```javascript

class BookStack {
  constructor() {
    this.stack = [];               // define a class BookStack and give it a constructor method that has one property
  }

  push(item) {
    return this.stack.push(item);  // add the item to the end of the array The array.push() method returns the new length array.
  }

  pop() {
    return this.stack.pop();       // remove the last item in the array, array.pop() method returns the item which was added,                                              // or undefined if the array is now empty
  }

  peek() {
    return this.stack[this.length - 1]; // we want to return, or peek at, the last item in the stack
  }

  get length() {                     // return length
    return this.stack.length;
  }

  isEmpty() {                        // return true if there are no items in the stack. So if the length is zero, return true.
    return this.length === 0;
  }
}

RESULT:

let myBookStack = new BookStack();
myBookStack.push('Oathbringer');
myBookStack.push('The Stand');
console.log(myBookStack.length); // 2
console.log(myBookStack.peek()); // The Stand
myBookStack.pop();
console.log(myBookStack.length); // 1
console.log(myBookStack.peek()); // Oathbringer
console.log(myBookStack.isEmpty()); // false
myBookStack.pop();
console.log(myBookStack.isEmpty()); // true

```

## Queue


A queue is similar to a stack in structure and methods, however the paradigm is different. 

Programmatically, Queues are just arrays with two primary operations: `unshift` and `pop`.

Queues use the “first-in-first-out” or “FIFO” method. This can be thought of like a queue, or line, of people waiting to buy movie tickets.

The person who’s been waiting the longest in line gets served before the person who just joined.

![Stack & Queue](https://res.cloudinary.com/practicaldev/image/fetch/s--_pp5Lukw--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/1600/1%2AA143SzcQuOhlZixXbFBpoA.png)

Queues leverage the following methods:

`enqueue(item)`: Add an item to the top of the queue

`dequeue()`: Remove the top item from the queue

`peek()`: Return the item at the top of the queue

`isEmpty()`: Returns true if the queue is empty

```javascript

class MovieQueue {
  constructor() {
    this.queue = [];
  }
 
  enqueue(item) {                       // add an item to the first index in an array (the back of the queue)
    return this.queue.unshift(item);
  }
 
  dequeue() {                           // remove the first item in the queue, or the last item in the array
    return this.queue.pop();
  }

  peek() {                              // see what the first item in the queue is, the last item in the array
    return this.queue[this.length - 1];
  }

  get length() {
    return this.queue.length;
  }

  isEmpty() {                           // return true if the queue is empty
    return this.queue.length === 0;
  }
}

RESULT:

const myMovieQueue = new MovieQueue();
myMovieQueue.enqueue('Sandra');
myMovieQueue.enqueue('Rob');
myMovieQueue.enqueue('Lisa');
myMovieQueue.enqueue('Kai');
console.log(myMovieQueue.length); // 4
console.log(myMovieQueue.peek()); // Sandra
myMovieQueue.dequeue();
myMovieQueue.dequeue();
console.log(myMovieQueue.peek()); // Lisa


```


## Linked List

Like arrays, `Linked Lists` store data elements in sequential order. 

Instead of keeping indexes, `linked lists` hold pointers to other elements. 

The first node is called the `head` while the last node is called the `tail`. 

In a singly-linked list, each node has only one pointer to the next node. In a doubly-linked list, a pointer to the previous node is also kept. Therefore, we can also start from the tail and walk “backwards” toward the head.

Like arrays, `linked lists` can operate as `stacks`. It’s as simple as having the head be the only place for insertion and removal. 

`Linked lists` can also operate as `queues`. This can be achieved with a doubly-linked list, where insertion occurs at the tail and removal occurs at the head, or vice versa. 

For large numbers of elements, this way of implementing queues is more performant than using arrays because `shift` and `unshift` operations at the beginning of arrays require linear time to re-index every subsequent element.

`Linked lists` are useful on both the client and server. On the client, state management libraries like `Redux` structure its middleware logic in a linked-list fashion. When `actions` are dispatched, they are piped from one middleware to the next until all is visited before reaching the `reducers`. On the server, web frameworks like `Express` also structure its middleware logic in a similar fashion. When a request is received, it is piped from one middleware to the next until a response is issued.

#### Another advantage of a linked list

In contrast to an array, which stores data contiguously in memory, a linked list can easily insert or remove nodes from the list without reorganization of the entire data structure.

#### Few drawbacks:

Random access of data elements is not allowed. Nodes must be accessed sequentially starting from the first one. Therefore, search operation is slow on a linked list.

It uses more memory than arrays because of the storage used by their pointers.

### Types of Linked lists

There are a few different types of linked lists. But the most popular ones are: `singly`, `doubly` and `circular`.

#### Singly linked list

![Singly](https://miro.medium.com/max/1369/1*Ftrp2Eg3-AuDpWa5Pe1fUQ.png)

Main operations on a linked list are: `insert` and `delete`.

- add(element) 
// It adds an element at the end of list.

- insertAt(element, index) 
// It inserts an element at the given index in a list.

- removeFrom(index) 
// It removes and returns an element from the list from the specified index

- removeElement(element) 
// This method removes element from the list. It returns the removed element, or if its not found it returns -1.

```js
1)
// User defined class node 

class Node { 
    // constructor 
    constructor(element) 
    { 
        this.element = element; 
        this.next = null
    } 
} 

2) 
// linkedlist class 

class LinkedList { 
    constructor() 
    { 
        this.head = null; 
        this.size = 0; 
    } 
  
    // functions to be implemented:
      // add(element) 
      // insertAt(element, location) 
      // removeFrom(location) 
      // removeElement(element) 
  
    // Helper Methods:
      // isEmpty 
      // size_Of_List 
      // PrintList 
} 
```

#### add(element)

```js
// adds an element at the end 
// of list 

add(element) 
{ 
    // creates a new node 
    var node = new Node(element); 
  
    // to store current node 
    var current; 
  
    // if list is Empty add the 
    // element and make it head 
    if (this.head == null) 
        this.head = node; 
    else { 
        current = this.head; 
  
        // iterate to the end of the 
        // list 
        while (current.next) { 
            current = current.next; 
        } 
  
        // add node 
        current.next = node; 
    } 
    this.size++; 
} 


In the order to add an element at the end of the list we consider the following :

- If the list is empty then add an element and it will be head
- If the list is not empty then iterate to the end of the list and add an element at the end of the list
current is used to iterate through the list after every iteration we update it to be the next of the current node. If next is null(the last element of a list contains null in the next) then we add the element to the list.

```

#### insertAt(element, index)

```js
// insert element at the position index of the list 

insertAt(element, index) 
{ 
    if (index > 0 && index > this.size) 
        return false; 
    else { 
        // creates a new node 
        var node = new Node(element); 
        var curr, prev; 
  
        curr = this.head; 
  
        // add the element to the 
        // first index 
        if (index == 0) { 
            node.next = head; 
            this.head = node; 
        } else { 
            curr = this.head; 
            var it = 0; 
  
            // iterate over the list to find 
            // the position to insert 
            while (it < index) { 
                it++; 
                prev = curr; 
                curr = curr.next; 
            } 
  
            // adding an element 
            node.next = curr; 
            prev.next = node; 
        } 
        this.size++; 
    } 
} 


In order to add an element at the end of the list we consider three conditions as follows:

- if the index is zero we add an element at the front of the list and make it head
- If the index is the last position of the list we append the element at the end of the list
- if the index is inbetween 0 or size – 1 we iterate over to the index and add an element at that index
In the above method prev holds the previous of current node.
```

#### removeFrom(index) 

```js
// removes an element from the specified location 

removeFrom(index) 
{ 
    if (index > 0 && index > this.size) 
        return -1; 
    else { 
        var curr, prev, it = 0; 
        curr = this.head; 
        prev = curr; 
  
        // deleting first element 
        if (index == = 0) { 
            this.head = curr.next; 
        } else { 
            // iterate over the list to the 
            // position to removce an element 
            while (it < index) { 
                it++; 
                prev = curr; 
                curr = curr.next; 
            } 
  
            // remove the element 
            prev.next = curr.next; 
        } 
        this.size--; 
  
        // return the remove element 
        return curr.element; 
    } 
} 

In order to remove an element from the list we consider three condition:

- If the index is 0 then we remove head and make next node head of the list
- if the index is size – 1 then we remove the last element form the list and make prev the last element
- if its in between 0 to size – 1 we remove the element by using prev and current node

```

#### removeElement(element)

```js
// removes a given element from the list 

removeElement(element) 
{ 
    var current = this.head; 
    var prev = null; 
  
    // iterate over the list 
    while (current != null) { 
        // comparing element with current 
        // element if found then remove the 
        // and return true 
        if (current.element == = element) { 
            if (prev == null) { 
                this.head = current.next; 
            } else { 
                prev.next = current.next; 
            } 
            this.size--; 
            return current.element; 
        } 
        prev = current; 
        current = current.next; 
    } 
    return -1; 
} 

The above method is just a modification of removeFrom(index), as it searches for an element and removes it, rather than removing from a specified location
```

