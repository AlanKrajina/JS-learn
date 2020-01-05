### Convert Celsius to Fahrenheit

```js
function convertToF(celsius) {
  let fahrenheit = celsius * (9/5) + 32;
  return fahrenheit;
}

convertToF(30);
```

### Reverse a String

```js
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```

### Factorialize a Number

For example: 5! = 1 * 2 * 3 * 4 * 5 = 120


```js
function factorialize(num) {
    var cnt = 1;
    for (var i = 1; i <= num ; i++) {
        cnt *= i;
    }
    return cnt;
}

factorialize(5)
```

### Find the Longest Word in a String

```js
function findLongestWordLength(str) {

  let newStr = str.split(' ').map(el => el.length)

  return newStr.sort(function(a, b){
    return a - b;
  }).pop()

}

findLongestWordLength("The quick brown fox jumped over the lazy dog");

// findLongestWordLength("What if we try a super-long word such as otorhinolaryngology") 

// 19

```

### Return Largest Numbers in Arrays

```js
function largestOfFour(arr) {
  let newArr;
  return newArr = arr.map(el=>
    el.sort(function(a, b){
    return a - b;
  }).pop()
  )
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);

// (4) [5, 27, 39, 1001]
```

### Confirm the Ending

Check if a string (first argument, str) ends with the given target string (second argument, target).
This challenge can be solved with the .endsWith() method, which was introduced in ES2015


```js
function confirmEnding(str, target) {
  
  let targetLetter = str.slice(-target.length)
  return targetLetter === target ? true : false 
}

confirmEnding("Bastian", "n");

OR

function confirmEnding(str, target) {

  return str.slice(str.length - target.length) === target;
}
```


### Repeat a String Repeat a String

Repeat a given string str (first argument) for num times (second argument). Return an empty string if num is not a positive number.
The built-in repeat() method should not be used.


```js
function repeatStringNumTimes(str, num) {
    let newStr = ''

    for(let i = 0; i < num; i++) { 
      newStr += str 
    }
    return newStr 
}

repeatStringNumTimes("abc", 3);

// "abcabcabc"
```

### Truncate a String

Truncate a string (first argument) if it is longer than the given maximum string length (second argument). Return the truncated string with a ... ending.


```js
function truncateString(str, num) {

   return str.length > num ? str.slice(0,num).concat('...') : str
}

truncateString("Peter Piper picked a peck of pickled peppers", 11) 
// "Peter Piper...".

truncateString("A-tisket a-tasket A green and yellow basket", "A-tisket a-tasket A green and yellow basket".length) 
// "A-tisket a-tasket A green and yellow basket".

truncateString("A-tisket a-tasket A green and yellow basket", "A-tisket a-tasket A green and yellow basket".length + 2) 
// "A-tisket a-tasket A green and yellow basket".
```

### Finders Keepers

Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.


```js
function findElement(arr, func) {

  return arr.find(el => func(el) )
}

findElement([1, 3, 5, 8, 9, 10], function(num) { return num % 2 === 0; }) 
// 8

findElement([1, 3, 5, 9], function(num) { return num % 2 === 0; }) 
// undefined
```

### Boo who

Check if a value is classified as a boolean primitive. Return true or false.


```js
function booWho(bool) {
  return typeof bool === "boolean" ? true : false
}

booWho(true) 
// true

booWho(false)
// true

booWho([1, 2, 3])
// false

booWho([].slice)
// false

booWho({ "a": 1 })
// false
```
