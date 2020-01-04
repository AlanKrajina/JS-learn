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

