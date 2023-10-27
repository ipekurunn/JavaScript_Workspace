# Introduction to JavaScript Array flatMap() method
The flatMap() method is used to convert each element within an array into another array using a function and make these subarrays into a single flattened array.

`array.flatMap(callback(currentValue[, index[, array]])[, thisArg])`

-**callback** function is run on each element and its return value must be a new array.

-**currentValue**

-**represents** the item the function is currently processing.

-**index (optional)** represents the index of the rendered element in the index.

-**array** (optional) represents the array being processed.

-**thisArg**(optional) specifies the this value used when calling the callback operation.

```javascript
let arr = [1, 2, 3, 4, 5];
let doubledArr = arr.flatMap(item => [item, item * 2]);

console.log(doubledArr); // [1, 2, 2, 4, 3, 6, 4, 8, 5, 10]
```
```javascript
let sentences = ["Hello, world!", "I love JavaScript."];
let words = sentences.flatMap(sentence => sentence.split(' '));

console.log(words); // ["Hello,", "world!", "I", "love", "JavaScript."]
```
Using the flatMap() method, it is very useful to manipulate arrays and transform them in another way.

