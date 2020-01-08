* [Convert Celsius to Fahrenheit](#Convert-Celsius-to-Fahrenheit)
* [Reverse a StringData types](#Reverse-a-String)
* [Factorialize a Number](#Factorialize-a-Number)
* [Find the Longest Word in a String](#Find-the-Longest-Word-in-a-String)
* [Return Largest Numbers in Arrays](#Return-Largest-Numbers-in-Arrays)
* [Confirm the Ending](#Confirm-the-Ending)
* [Repeat a String Repeat a String](#Repeat-a-String-Repeat-a-String)
* [Truncate a String](#Truncate-a-String)
* [Finders Keepers](#Finders-Keepers)
* [Boo who](#Boo-who)
* [Title Case a Sentence](#Title-Case-a-Sentence)
* [Slice and Splice](#Slice-and-Splice)
* [Falsy Bouncer](#Falsy-Bouncer)
* [Where do I Belong](#Where-do-I-Belong)
* [Mutations](#Mutations)
* [Chunky Monkey](#Chunky-Monkey)


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
    let cnt = 1;
    for (let i = 1; i <= num ; i++) {
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

findLongestWordLength("What if we try a super-long word such as otorhinolaryngology") 

// 19


function findLongestWordLength(str) {
  let newStr = str.split(' ')

  return newStr.sort(function(a, b){
    return a.length - b.length;
  }).pop()
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");

// jumped

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

### Title Case a Sentence

Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.


```js
function titleCase(str) {

  let newStr =  str.toLowerCase().split(' ')

  return newStr.map(el=> 
    el.charAt(0).toUpperCase().concat(el.slice(1))
    ).join(' ')
}

titleCase("I'm a little tea pot") 
// string

titleCase("I'm a little tea pot") 
// I'm A Little Tea Pot.

titleCase("sHoRt AnD sToUt") 
// Short And Stout.
```

### Slice and Splice

Use the array methods slice and splice to copy each element of the first array into the second array, in order.
Begin inserting elements at index n of the second array.
Return the resulting array. The input arrays should remain the same after the function runs.

```js
function frankenSplice(arr1, arr2, n) {

  let newArr = arr2
  newArr.splice(n,0,arr1)

  return newArr.flat()
}

frankenSplice([1, 2, 3], [4, 5], 1) 
// [4, 1, 2, 3, 5].

frankenSplice([1, 2], ["a", "b"], 1) 
// ["a", 1, 2, "b"].
```

### Falsy Bouncer

Remove all falsy values from an array.
Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.

```js
function bouncer(arr) {

  return arr.filter(el=> !!el )
}

bouncer([7, "ate", "", false, 9]) 
// [7, "ate", 9]

bouncer(["a", "b", "c"]) 
// ["a", "b", "c"]

bouncer([false, null, 0, NaN, undefined, ""]) 
// []

bouncer([null, NaN, 1, 2, undefined]) 
// [1, 2]
```

### Where do I Belong

Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).

```js
function getIndexToIns(arr, num) {
  
  arr.push(num);
  arr.sort(function(a, b) {
    return a - b;
  });
  return arr.indexOf(num);
}

getIndexToIns([2, 20, 10], 19)
// 2

getIndexToIns([2, 20, 10], 19)
// number

getIndexToIns([2, 5, 10], 15)
// 3

getIndexToIns([2, 5, 10], 15) 
// number

getIndexToIns([], 1) 
// 0
```

### Mutations

Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.

The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".

Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".

```js
function mutation(arr) {
  return arr[1]
    .toLowerCase()
    .split("")
    .every(function(letter) {
      return arr[0].toLowerCase().indexOf(letter) != -1;
    });
}

// Every will basically give you letter by letter to compare, which we do by using indexOf on the first string. 

// indexOf will give you -1 if the current letter is missing. 

// We check that not to be the case, for if this happens even once every will be false.


mutation(["hello", "hey"])
// false

mutation(["hello", "Hello"])
// true

mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"])
// true

mutation(["Mary", "Army"])
// true

mutation(["Mary", "Aarmy"])
// true

mutation(["Alien", "line"])
// true

mutation(["floor", "for"])
// true
```

### Chunky Monkey

Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

```js
function chunkArrayInGroups(arr, size) {
  const chunked_arr = [];
  let index = 0;
  while (index < arr.length) {
    chunked_arr.push(arr.slice(index, size + index));
    index += size;
  }
  return chunked_arr;
}


chunkArrayInGroups(["a", "b", "c", "d"], 2) 
// [["a", "b"], ["c", "d"]].

chunkArrayInGroups([0, 1, 2, 3, 4, 5], 3) 
// [[0, 1, 2], [3, 4, 5]].

chunkArrayInGroups([0, 1, 2, 3, 4, 5], 2) 
// [[0, 1], [2, 3], [4, 5]].
```
