# Introduction to the JavaScript Array includes() method
The includes() method checks whether an array contains a particular element. Returns true if the element is found in the array, returns false if not.

`array.includes(element, fromIndex);` 

-**element:** The element to search for in the array.

-**fromIndex** (optional):The index location to start the search. If not specified, the search starts from the beginning of the array.
```javascript
[1,2,3].includes(2); // true
[1,2,3].includes(4); // false
[1,2,3].includes(1,1); // false
```
**Working with NaN:**
```javascript
[NaN].includes(NaN); // true
```
**+0 and -0 difference is not taken into consideration:**
```javascript
[-0].includes(+0); // true
```
**Checking if object exists in array:**
```javascriptlet bmw = {name: 'BMW' }, 
    toyota = { name: 'Toyota'},
    ford = {name: 'Ford'}

let cars = [ford, toyota];

console.log(cars.includes(ford)); // true
console.log(cars.includes(bmw)); // false
```
It returns false because the bmw object is not in the array.

