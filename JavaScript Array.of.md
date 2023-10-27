# Introduction to the JavaScript Array.of() method
Array.of() method is used to solve some problems encountered in ES5.

In ES5, when passing a number to the Array constructor, JavaScript creates an array with the length of the number:
```javascript
var numbers = [1, 2, 3, 4, 5];
var newNumbers = numbers.slice();
```
However, when passing a non-number value to the Array structure, JavaScript creates an array with that value:
```javascript
numbers = new Array("2");
console.log(numbers.length); // 1
console.log(numbers[0]); // "2"
```
This behavior is sometimes confusing and error prone because you may not know the type of data you are passing into the Array structure.

The Array.of() method always creates an array containing the values you pass, no matter what type or how many arguments you pass:
```javascript
let numbers = Array.of(3);
console.log(numbers.length); // 1
console.log(numbers[0]); // 3
```
```javascript
let chars = Array.of('A', 'B', 'C');
console.log(chars.length); // 3
console.log(chars); // ['A','B','C']
```















