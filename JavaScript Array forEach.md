# Introduction to JavaScript Array forEach() method
In JavaScript, the forEach() method is used to process each element within an array. This method calls a function for each element in the array.
```javascript
array.forEach(function(currentValue, index, array) {
    // The operations to be performed on each item are defined here
});
```
-**array:** Represents the array on which the forEach() method is called.

-**currentValue:** Represents the array element in the current operation.

-**index:** Represents the index of the current item in the array.
```javascript
let colors = ["red", "green", "blue"];

colors.forEach(function(color, index) {
    console.log("Renk " + index + ": " + color);
});
```
Output:
`Renk 0: red
Renk 1: green
Renk 2: blue
`


