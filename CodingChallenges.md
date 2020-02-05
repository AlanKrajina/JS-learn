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

### Compare Triplets

```js
let arr1 = [1,3,3]
let arr2 = [3,2,1]

function compareTriplets(a, b) {
    let score = [0,0]

    for (let i = 0; i < a.length; i++)                              // i = value is 0,1,2 
        a[i] > b[i] ? score[0]++ : a[i] < b[i] ? score[1]++ : ""
    return score
}

compareTriplets(arr1, arr2)
```
