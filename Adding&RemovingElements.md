# Introduction to the JavaScript Array push() method
The `Array.prototype.push()` method adds one or more elements to the end of an array and returns the length of the new array.

This method is used with the following syntax:
```javascript
push(newElement);
push(newElement1, newElement2);
push(newElement1, newElement2, ..., newElementN);
```
The `push()` method returns the new value of the length property of the array object on which the method is called.
## JavaScript Array push() method examples
### 1-Adding a single element to an array
```javascript
let numbers = [21, 30, 55];
const length = numbers.push(18);
console.log(length);
console.log(numbers);
```
Output:
```
4
[21, 30, 55, 18]
```
### 2-Adding multiple elements to an array
```javascript
let numbers = [21, 30, 55];
const length = numbers.push(18, 45);
console.log(length);
console.log(numbers);
```
Output:
```
4
[21, 30, 55, 18, 45]
```
### 3-Adding elements of one array to another array
There are 2 methods to add elements of one array to another array.

`for...of` loop or ES6's span operator (`...`):

```javascript
let colors = ['purple', 'orange', 'black'];
let cmyk = ['cyan', 'magenta', 'yellow', 'black'];
// with for...of loop
for (const color of cmyk) {
  colors.push(color);
}
// with span operator
colors.push(...cmyk);

console.log(colors);
```
Output:
```
['purple', 'orange', 'black', 'cyan', 'magenta', 'yellow', 'back']
```
## Using JavaScript Array push() method with array-like objects
In JavaScript, an array-like object is an object of a structure that resembles an array. These objects typically emulate an array, but may not have array methods or properties. Typically, such objects have a length property, but they do not have array methods or other array-specific properties.

The push() method is used to add elements to the array, and this method essentially uses the length property of the array. Therefore, the push() method can also be used on an array-like object.
```javascript
let greetings = {
  0: 'Hi',
  1: 'Hello',
  length: 2,
  append(message) {
    [].push.call(this, message);
  },
};
greetings.append('Howdy');
greetings.append('Bonjour');

console.log(greetings);
```
This code creates an object named `greetings`. This object has indexes such as `0` and `1`, and its `length` property is set to `2`. This object has an array-like structure.

A method called `append()` is also defined. This method adds new elements to the `greetings` object using the `push()` method. The `push()` method is called as `[].push.call(this, ...arguments)`to operate on this object. Here's how this example works:

1. `greetings.append('Howdy', 'Bonjour');` When the line is called, the `append` method starts working.

2. The `append` method adds an element to the `greetings` object by calling the `push()` method. The `...arguments` statement separates all the arguments passed to the append method (i.e. `Howdy` and `Bonjour`) and appends these elements via the `push()` method.

3. The `push()` method automatically updates the length property when adding elements to the `greetings` object. The `length` property reflects the number of added elements. Originally the `length` was 2, but since we added two elements the `length` is now 4.

4. `console.log(greetings);` The line prints the `greetings` object to the console. The result is that the `greetings` object will look like this:

Output:
```
{
  '0': 'Hi',
  '1': 'Hello',
  '2': 'Howdy',
  '3': 'Bonjour',
  length: 4,
  add: [Function: add]
}
```
## Summary
-Use the JavaScript array push() method to append one or more elements to an array.

-The push() method also works with an array-like object.


