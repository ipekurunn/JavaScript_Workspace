# Introduction to JavaScript array filter() method
The filter() method is used to select elements in an array that meet a certain condition and create a new array containing those elements.

`newArray = array.filter(callback(element[, index[, array]])[, thisArg])`

-**newArray:** The newly created array contains the elements of the original array that meet a certain condition.

-**callback:** This is a function that processes each array element. The function takes three arguments: element (the current element), index (the index number of the current element), and array (the array on which the filter() method is called).

-**thisArg** (optional): This specifies the "this" value to use within the function.
```javascript
let numbers = [10, 20, 30, 40, 50, 60];
let evenNumbers = numbers.filter(function (number) {
    return number % 2 === 0;
});
```
This code tests each element in the array with the filter() method and creates a new array, evenNumbers, that contains only even numbers.

**Arrow Fonksiyon Kullanımı:**
```javascript
let numbers = [10, 20, 30, 40, 50, 60];
let evenNumbers = numbers.filter(number => number % 2 === 0);
```
**Warning!** The filter() method returns a new array containing elements that meet a given condition, and the original array is not modified.














