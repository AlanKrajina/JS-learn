### Sum All Numbers in a Range

```js
function sumAll(arr) {

  let newArr = arr.sort(function(a,b){
    return a - b
  })
    let lastDigit = newArr[newArr.length -1]
    let firstDigit = newArr[0];
    let numb = 0

    for (let i = firstDigit; i <= lastDigit ; i++) {
        numb += i;
    }
    return numb;

}

sumAll([1, 4]) 
// number

sumAll([1, 4]) 
// 10

sumAll([4, 1]) 
// 10

```

