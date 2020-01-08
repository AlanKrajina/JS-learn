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
