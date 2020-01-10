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
// [4]

["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// ["pink wool"].

["diorite", "andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// array with one item.

["andesite", "grass", "dirt", "pink wool", "dead shrub"], ["diorite", "andesite", "grass", "dirt", "dead shrub"] 
// ["diorite", "pink wool"].

```

### Seek and Destroy

You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. 

Remove all elements from the initial array that are of the same value as these arguments.

You have to use the arguments object.


```js
function destroyer(arr) {

  // arr = [ 1, 2, 3, 1, 2, 3 ]

  // console.log(arguments)
  // [Arguments] { '0': [ 1, 2, 3, 1, 2, 3 ], '1': 2, '2': 3 }

  // convert arguments into array:
  // let args = Array.prototype.slice.call(arguments);
  // [ [ 1, 2, 3, 1, 2, 3 ], 2, 3 ]
  
  
  let args = Array.from(arguments).slice(1); // take 2,3 from arguments -> [ 2, 3 ]
  return arr.filter(val=>
     !args.includes(val))   // checking each arr value in args array and returning not included value
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3) 
// [1, 1]

destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3) 
// [1, 5, 1]

destroyer([3, 5, 1, 2, 2], 2, 3, 5) 
// [1]

destroyer([2, 3, 2, 3], 2, 3) 
// []

```

### Wherefore art thou

Make a function that looks through an array of objects (first argument) and returns an array of all objects that have matching name and value pairs (second argument). 

Each name and value pair of the source object has to be present in the object from the collection if it is to be included in the returned array.

For example, if the first argument is [{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], and the second argument is { last: "Capulet" }, then you must return the third object from the array (the first argument), because it contains the name and its value, that was passed on as the second argument.


```js
function whatIsInAName(collection, source) {

  let srcKeys = Object.keys(source);

  // filter the collection
  return collection.filter(obj => {
    return srcKeys
      .map(key => {
        return obj.hasOwnProperty(key) && obj[key] === source[key];
      })
      .reduce((a,b) => {
        return a && b;
      });
  });
}


whatIsInAName([{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], { last: "Capulet" }) 
// [{ first: "Tybalt", last: "Capulet" }]

whatIsInAName([{ "apple": 1 }, { "apple": 1 }, { "apple": 1, "bat": 2 }], { "apple": 1 }) 
// [{ "apple": 1 }, { "apple": 1 }, { "apple": 1, "bat": 2 }]

whatIsInAName([{ "apple": 1, "bat": 2 }, { "bat": 2 }, { "apple": 1, "bat": 2, "cookie": 2 }], { "apple": 1, "bat": 2 }) 
// [{ "apple": 1, "bat": 2 }, { "apple": 1, "bat": 2, "cookie": 2 }]

```
