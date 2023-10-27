# Introduction to JavaScript Array at() Method
Normally in JavaScript, arr[] is used to access the element of an array. arr[0] to the first element, arr[1] to the 2nd element, etc.

But to get to the last element in JavaScript

We cannot use arr[-1]. It returns undefined.`arr[lenght-1]` is used instead.

`arr.at(index)`

Here 0, negative or positive can be used.
```javascript
const scores = [5, 6, 7];

console.log(scores.at(1)); // same as scores[1] 

// get the last element
console.log(scores.at(-1)); // 7

console.log(scores.at(-1) === scores[scores.length - 1]); // true
```
Output:

```
6
7
true
```
