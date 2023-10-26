# Introduction to JavaScript Array every() method
The every() method is used to check whether all elements in an array meet a certain condition. every() returns true if all elements in the array satisfy a certain condition. Otherwise, it returns false.

`array.every(callback(currentValue[, index[, array]])`

-**callback:** This is a function that checks each array element. The function takes three arguments:

-**currentValue:** Current item.

-**index** (optional): The index number of the current item.

-**array** (optional): The array on which the every() method is called.
```javascript
let numbers = [1, 2, 3, 4, 5];
let allEven = numbers.every(function (currentValue) {
    return currentValue % 2 === 0;
});
```
This code checks each element in a single line and checks if all elements are even numbers.

The every() method returns a boolean value (true or false) as the result. If all elements meet certain condition, the result will be true, otherwise false.

**Arrow Function Usage:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let allEven = numbers.every(currentValue => currentValue % 2 === 0);
```
