# Introduction to JavaScript Array Array.from() method
The Array.from() method allows you to create a new array using an array-like object or iteration. This is very useful for extracting or manipulating your data in different formats.

`Array.from(iterable, mapFn, thisArg)`

-**iterable:** This must be an array-like object or iteration. That is, this object can be traversed (for example, an array, a Set, a Map, a String, or an iteration). Array.from() creates a new array using this object.

-**mapFn** (optional): This can be a mapping function that will be used to add each element to the array. This function is run on each element and adds the processed data to the array. If you do not specify this parameter or leave it as null or undefined, an array containing the same elements is returned without any conversion.

-**thisArg** (optional): Sets the this value used by mapFn. This is useful when you need to use this inside the function.

## 1-Converting an array-like object to an array
```javascript
let set = new Set([1, 2, 3, 4, 5]);
let arr = Array.from(set);
console.log(arr); // [1, 2, 3, 4, 5]
```
## 2-Converting string to character array
```javascript
let str = 'Hello';
let chars = Array.from(str);
console.log(chars); // ['H', 'e', 'l', 'l', 'o']
```
## 3-Act on each item
```javascript
let numbers = [1, 2, 3];
let doubled = Array.from(numbers, num => num * 2);
console.log(doubled); // [2, 4, 6]
```
