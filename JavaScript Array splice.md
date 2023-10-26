# JavaScript Array splice: Delete, Insert, and Replace
## 1-Deleting Elements
`Array.splice(position,num);`
**position** specifies the position of the first item to be deleted.
**num** determines the number of items to delete.
```javascript
let numbers = [1, 2, 3, 4, 5];
let deletedNumbers = numbers.splice(0, 3);

console.log(numbers);  //[4, 5]
console.log(deletenNumbers);  //[1, 2, 3]
```
In this example, the scores array contains five numbers, and the splice(0, 3) statement deletes the first three elements of the array.
## 2-Inserting Elements
We can use splice() method to add one or more elements.
```javascript
let colors = ['blue', 'purple', 'orange']
colors.splice(2, 0, 'red', 'pink', 'green');

console.log(colors);  //["blue", "purple", "red", "pink", "green", "orange]
```
`Note:` Here, 2 represents the index from which items will be added.
0 represents the items to be deleted. Since we did not delete any element here, we wrote it as 0.
## 3-Replacing Elements
```javascript
let colors = ['blue', 'purple', 'orange', 'yellow']
colors.splice(1, 1, 'black');

console.log(colors);  //["blue", "black", "orange", "yellow"]
```
In this example, it goes to index 1, deletes 1 element, and replaces it with the element 'black'.

At the same time, we can add more arguments to replace multiple elements:
```javascript
let colors = ['blue', 'purple', 'orange', 'yellow']
colors.splice(2, 1, 'black', 'white', 'red');

console.log(colors);  //["blue", "purple", "black", "white", "red", "yellow"]
```









