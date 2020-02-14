http://overapi.com/nodejs

https://nikgrozev.com/2017/01/22/node-js-cheatsheet-part-1/

### Non-Blocking Input/Output

With Rails the slowness is due to the high-level of abstraction which means that the Object Relational Mapper (ORM) Active Record and the framework as a whole is doing too many things. It's a good thing for developers because we have to code less, but as real-life shows, it's not so good for the systems.

The approach is called `blocking input/output (I/O)` in computer world because the line(s) are blocked by previous orders (or tasks in the computer lingo). The line is a metaphor for a queue of tasks while the employees can be servers. So how is Node.js different? Node.js has `non-blocking I/O` which as you might guess is the latter approach.

The queue moves, and the processes are executed asynchronously and without blocking the queue. 

For example, a `Node.js` server can process a request from client B while it waits for a response from a database to serve a response to client A. Most other systems will do nothing while they wait for a reply from a database to serve client A's request.

-> the idea is that you can re-use files, libraries and modules between the server and the browser seamlessly.

### REPL

`REPL` stands for `read-evaluate-print loop` and does exactly what you would expect. It takes your command, executes it and prints the result if any. It looks similar to a command prompt or a terminal, but with an angle bracket > instead of the dollar $ or some other command prompt sign.

`REPL` is as an environment in which we can run Node code. Many other languages and platforms also have a similar REPL environment. Browser JavaScript can be run in the console of Google Chrome DevTools. You should be familiar with a REPL from using the Ruby-REPL irb.

##### USING (JS irb)

```js
// in terminal or cmd type:

node

// then:

> 1+1
2

> function adder(){return 1 + 1}
undefined
> adder()
2

// exiting

> .exit
```
