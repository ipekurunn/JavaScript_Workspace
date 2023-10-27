# Introduction to the JavaScript Array flat() method
The flat() method is used to convert a multidimensional array into a single-dimensional array by concatenating nested subarrays.

`array.flat([depth])`

-**The depth** (optional) parameter determines how many levels deep you should merge nested arrays. By default it is set to 1 and only merges one level of nested arrays.

-**flat()** method merges all nested arrays at the specified depth level and returns a new array
```javascript
var numbers = [1, 2, 3, 4, 5];
var newNumbers = numbers.slice();
```
## 1-A simple usage
```javascript
let arr = [1, 2, [3, 4]];
let flatArr = arr.flat();

console.log(flatArr); // [1, 2, 3, 4]
```
## 2-Merge at a specific depth level
```javascript
let arr = [1, 2, [3, [4, 5]]];
let flatArr = arr.flat(2);

console.log(flatArr); // [1, 2, 3, 4, 5]
```
## 3-Not indicating depth level
```javascript
let arr = [1, [2, [3, [4, [5]]]]];
let flatArr = arr.flat();

console.log(flatArr); // [1, 2, [3, [4, [5]]]]
```
`Note:` If you don't specify the depth level when using flat(), it will only be merged into one level depth by default.
