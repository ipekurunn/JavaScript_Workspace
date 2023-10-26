# Introduction to JavaScript Array map() method
The map() method is used to process each element of an array and return a new value for each element. That is, it operates on the original array and creates a new array as a result.

`newArray = array.map(callback(element[, index[, array]])[, thisArg])`

-**newArray:** The newly created array contains a rendered version of each element of the original array.

-**callback:** This is a function that processes each array element. The function takes three arguments: element (the current element), index (the index number of the current element), and array (the array on which the map() method is called).

-**thisArg** (optional): This specifies the "this" value to use within the function.
```javascript
let numbers = [1, 2, 3, 4, 5];
let squaredNumbers = numbers.map(function (number) {
    return number * number;
});
```
This code squares each element with the map() method and adds the result to the squaredNumbers array. 

As a result, the squaredNumbers array becomes: [1, 4, 9, 16, 25].

**Arrow Function Usage:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let squaredNumbers = numbers.map(number => number * number);
```


























