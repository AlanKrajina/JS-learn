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

`Push` adds elements to the top of the array, while `Pop` removes them from the same location. In other words, Stacks follow the “Last In, First Out” protocol (LIFO).
Below is an example of a Stack in code. Notice that we can reverse the order of the stack: the bottom becomes the top and the top becomes the bottom. As such, we can use the array’s unshift and shift methods in place of push and pop, respectively.


#### Push
```javascript

Adds an element to the stack.
// This method adds an element at the top of the stack.

// push function: 

push(element) 
{ 
    // push element into the items 
    this.items.push(element); 
} 
```

#### Pop()
```javascript

Removes an element from the stack, if the function is call on an empty stack it indicates “Underflow”.
// This method returns the topmost element of stack and removes it. Return underflow when called on an empty stack.


// pop function:

pop() 
{ 
    // return top most element in the stack 
    // and removes it from the stack 
    // Underflow if stack is empty 
    if (this.items.length == 0) 
        return "Underflow"; 
    return this.items.pop(); 
} 

```

#### Peek()
```javascript

Returns the top most elements in the stack, but doesn’t delete it.
// Return the topmost element without removing it from the stack.

// peek function:

peek() 
{ 
    // return the top most element from the stack 
    // but does'nt delete it. 
    return this.items[this.items.length - 1]; 
} 
```
