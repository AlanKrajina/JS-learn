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

### A Very Big Sum

Example 1.
```js
let ar = [1000000001,1000000002,1000000003,1000000004,1000000005]

function aVeryBigSum(ar) {
    return ar.reduce((target, item) => {
        return target + item;
    }, 0);
}

// 5000000015
```

Example 2.
```js
let arr = ['5', '1000000001 1000000002 1000000003 1000000004 1000000005']

function aVeryBigSum(arr) {

  let newArr = arr[1].split(' ').map(el=> parseInt(el))
  return newArr.reduce((a,b)=> a+b)
}

// 5000000015
```
