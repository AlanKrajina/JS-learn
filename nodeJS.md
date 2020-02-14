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

### Launching Node

The `program.js` is a plain text file with a `.js` extension. To run this program, we go to terminal, navigate to the folder with the script, and run this command:

```js
node program.js

// or

node program
```

If you are not in the same folder as your script file, you can navigate to it or specify path:

```js
node /Users/azat/Documents/Code/learn-co/program.js
```

List of node CLI commands:

```js
node -h
```
```js
-v, --version          //: print Node.js version
-e, --eval script      //: evaluate script
-p, --print            //: evaluate script and print result
-c, --check            //: syntax check script without executing
-i, --interactive      //: always enter the REPL even if stdin does not appear to be a terminal
-r, --require          //: module to preload (option can be repeated)
--no-deprecation       //  silence deprecation warnings
--throw-deprecation    //  throw an exception anytime a deprecated function is used
--trace-deprecation    //  show stack traces on deprecations
--trace-sync-io        //  show stack trace when use of sync IO is detected after the first tick
--track-heap-objects   //  track heap object allocations for heap snapshots
--v8-options           //  print v8 command line options
--tls-cipher-list=val  //  use an alternative default TLS cipher list
--icu-data-dir=dir     //  set ICU data load path to dir (overrides NODE_ICU_DATA)
```

##### Use node CLI command options and flags to launch node scripts in different modes

Run the code from a command-line:

```js
node -e "console.log(new Date)"

// 2020-02-14T16:48:11.238Z
```
Pattern:

node [options] [ -e script | script.js ] [arguments]

Where square brackets [] mean optional parameters. The [options] can be a single option like -v, or a combination of options listed by the help command. script.js is a file with the code to execute. We can also run code from a string (-e).

And the argument is the data to pass to the script. We can pass multiple argument separating them with spaces. 

### Mocha Testing Framework

This lesson will cover the basics of Mocha testing framework and Chai Expect behavioral-driven language.

```js
npm install mocha@2.4.5 --save-dev
npm install chai@3.5.0 --save-dev
```

##### TEST

```js
var expect = require('chai').expect
var name = 'React Quickly'
var url = ['http://reactquickly.co', 'https://www.manning.com/books/react-quickly']

describe('name and url', function() {
  it('must match the values', function(done){
    expect(name).to.be.a('string')
    expect(name).to.equal('React Quickly')
    expect(url).to.have.length(2)
    expect(url).to.have.deep.property('[1]', 'https://www.manning.com/books/react-quickly')
      .with.length(43)
    done()
  })
})
```

##### Launching Mocha Tests

There are two ways to run Mocha tests: local and global.

Local in terminal:
```js
node_modules/mocha/bin/mocha test.js
```

### Hello World Lab (exporting .js file)

https://stackabuse.com/how-to-use-module-exports-in-node-js/

```js
npm install
npm test
```

```js
// expression:

const helloWorld = () => {
  return 'Hello World'
}

module.exports = helloWorld
```

### Node Debugger

https://learn.co/tracks/introduction-to-node-js/intro-to-node-js/node-basics/node-debugger

```js
node inspect program.js
```

##### Debugger Commands

```js
run                    // run program
cont (c)               // continue, i.e., proceed with the execution until a breakpoint
next (n)               // step to the next line
step (s)               // step in (go deeper into the execution context)
out (o)                // step out (go out of the execution, skipping the deeper context)
setBreakpoint (sb)     // put the break point, e.g., setBreakpoint(20) sets the break point on line 20
clearBreakpoint (cb)   // remove the break point, e.g., clearBreakpoint('script.js', 1) clears the break point in thescript.js` file on                           line 1.
```


