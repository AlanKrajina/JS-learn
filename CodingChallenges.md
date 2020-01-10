### Check if a number is square

```js
let isSquare = function(n){
  
  return Math.sqrt(n) % 1 === 0;
}

isSquare(-1) 
// false
isSquare(0)
// true
isSquare(3)
// false
isSquare(4)
// true
isSquare(25)
// true  
isSquare(26)
// false

// The sqrt() method returns the square root of a number.

```
