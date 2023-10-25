# JavaScript Array Length
At its core, the length property of an array is an **unsigned**, **32-bit integer**. Its primary function is to represent the number of elements in the array and is always **numerically greater than the highest index** in the array. To put it simply, the length property tells you how many items are in your array, but it also behaves differently based on the type of array you're dealing with.

The value of the length is 232. It means that an array can hold up to 4294967296 (232) elements.

## 1-Dense Arrays
In dense arrays, the length property gives the number of elements in the array.
```javascript
let colors = ['purple', 'blue', 'orange'];
console.log(colors.length);  //3
```
In the example above, the length of the colors array is three because there are three elements in the array. 

When you add a new element to the array using the push method, the length property is automatically updated.
```javascript
colors.push('green');
console.log(colors.length);  //4
```
When you empty the colors array, its length is zero:
```javascript
colors = []
console.log(colors.length);  //0
```
## 1-Sparse Arrays
Sparse arrays are non-consecutive arrays whose element indexes start from zero. In other words, sparse arrays have gaps or missing indices between elements. This means that some indexes are unassigned or missing within the array.

For example, the following array represents a sparse array:
```javascript
let numbers = [9, , 32, 21];
```
While this array contains values such as 9 at index 0, 32 at index 2, and 21 at index 3, the value at index 1 appears to be unassigned. This means the array is sparse. In sparse arrays, elements with missing indexes are still part of the array, but are considered "undefined" if no values are assigned to those indexes.

An important property of sparse arrays is that the length property of the array does not reflect the actual number of elements. The array length is always a number greater than the highest index in the array. This should be taken into account when calculating the actual number of elements of the array.

In summary, sparse arrays are arrays that have gaps or omissions between indexes, and the length property does not reflect the actual number of elements of the array. Therefore, when working with sparse arrays, it is important to accurately keep track of whether indexes have been assigned and the actual number of elements of the array.

```javascript
let numbers = [9, , 32, 21];
numbers[10] = 100;
console.log(numbers.length);  //11
```
In the example above, the 10th index of the number array is assigned the value 100. As we said, the length property always represents a number greater than the highest index in the array. Since we assigned a value to the 10th index here, the length property has now increased by 11.

# Modifying JavaScript Array Length Property
## 1-Empty an Array
If you set length to zero, the array will be empty:
```javascript
const fruits = ['Strawberry, 'Mango', 'Cherry'];
fruits.length = 0;

console.log(meyveler);  // []
```
## 2-Remove Elements
If you set the length of the array to a value equal to or greater than the highest index, all elements with an index equal to or greater than the new length are removed.
```javascript
const fruits = ['Strawberry, 'Mango', 'Cherry'];
fruits.length = 2;

console.log(meyveler);  // ['Strawberry, 'Mango']
```
## 3-Make Array Sparse
If you set the length of the array to a value greater than the highest index, the array becomes sparse.
```javascript
const fruits = ['Strawberry, 'Mango', 'Cherry'];
fruits.length = 2;

console.log(meyveler);  // ['Strawberry, 'Mango', 'Cherry', , ]
```
## Summary
-The length of an array is a 32-bit integer that is always greater than the highest index in the array.

-In dense arrays, length returns the number of elements in the array.

-In sparse arrays, the length does not reflect the actual number of elements in the array.

-Changing the length property can remove elements from the array or make the array sparse.





