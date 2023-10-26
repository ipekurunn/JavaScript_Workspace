# Introduction to JavaScript Array sort() method
The sort() method is used to sort the elements in an array. Sorting can perform items in alphabetical order or numerical order.

`array.sort([compareFunction])`

**compareFunction** (optional): This is a function that represents the comparison function. The function compares two elements and is used to change the position of the elements during sorting. If this function is not specified, the elements are sorted alphabetically and the array is replaced in place.

```javascript
let fruits = ["banana", "apple", "mango", "cherry"];
fruits.sort();
```
Output:
`["apple", "banana", "cherry", "mango"]`

**compareFunction Usage:**

compareFunction takes parameters a and b that represent both elements. This function compares these two elements by returning a - b. If a - b returns a negative value, a comes before b and therefore comes first in the sorting.
```javascript
let numbers = [10, 2, 8, 6, 4];
numbers.sort(function (a, b) {
    return a - b;
});
console.log(numbers);
```
Output:
`[2, 4, 6, 8, 10]`
```javascript
let numbers = [10, 2, 8, 6, 4];
numbers.sort(function (a, b) {
    return b - a;
});
console.log(numbers);
```
Output:
`[10, 8, 6, 4, 2]`
