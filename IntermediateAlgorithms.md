### Sum All Numbers in a Range

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. The lowest number will not always come first.

For example, sumAll([4,1]) should return 10 because sum of all the numbers between 1 and 4 (both inclusive) is 10.

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


### Diff Two Arrays

Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. 

In other words, return the symmetric difference of the two arrays.


```js
function diffArray(arr1, arr2) {
  return arr1
    .concat(arr2)
    .filter(item => !arr1.includes(item) || !arr2.includes(item));
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]) 
// array

["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// ["pink wool"].

["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// array with one item.

["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// ["diorite", "pink wool"].

```
