# Introduction to the JavScript Array unshift() method
The Array.prototype.unshift() method adds one or more elements to the beginning of an array and returns the length of the new array. 

This method is used with the following syntax:
```javascript
unshift(newElement);
unshift(newElement1, newElement2);
unshift(newElement1, newElement2, ..., newElementN);
```
**Warning!** The `push()` method adds to the end of the array, while the `unshift()` method adds it to the beginning of the array. The two should not be confused.

**Note:** The `unshift()` method is slow if there are many elements in the array because it must reindex all existing elements.

## 1-Adding an element to an array
```javascript
let numbers = [30, 55];
const length = numbers.unshift(21);
console.log({length});
console.log({numbers});
```
Output:
```
{length: 3}
{numbers: [21, 30, 55]}
```
## 2-Adding multiple elements to an array
```javascript
let numbers = [30, 55];
const length = numbers.unshift(21, 42);
console.log({length});
console.log({numbers});
```
Output:
```
{length: 4}
{numbers: [21, 42, 30, 55]}
```
## 3-Adding elements of one array to another array
There are 2 methods to add elements of one array to another array.
```javascript
let days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];
let weekends = ['Saturday', 'Sunday'];
// with for...of loop
for (const weekend of weekends) {
  days.unshift(weekend);
}
// with span operator
days.unshift(...weekends);

console.log(days);
```
Output:
```
['Sunday', 'Saturday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']
```
## 4-Using the JavaScript Array unshift() method with array-like objects

In this example, we create an object named `
greetings`. This object has elements with indexes such as 0, 1 and 2, and its length property is set to 3. This object represents an array-like object.

A method called prepend() is also defined. This method adds a new message to the beginning of the object using the unshift() method. Since the prepend() method operates on an array-like object, it calls the unshift() method on this object using [].unshift.call(this, message).

In the example, calling greetings.prepend('Good day') invokes the prepend() method and adds a new message named 'Good day' to the beginning of the greetings object.

As a result, the elements of the greetings object are updated successfully and the length property is automatically updated to 4.
## Summary
-The JavaScript array unshift() method is used to add one or more elements to the beginning of an array.

-The unshift() method also works with array-like object using call() or apply() method.







