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
