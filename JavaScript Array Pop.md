# Introduction to the JavaScript Array pop() method
```javascript
array.pop()
```
`Note:` The pop() method changes the length property of the array. If the array is empty, the pop() returns undefined.
## 1-Removing the last element from an array
```javascript
const myArray = [10, 20, 30];
const removedElement = myArray.pop();

console.log(removedElement);  //30
console.log(myArray.lenght);  //2
```
Output:
```
30
2
```
In this example, the pop() method removes the number 30 from the myArray. Because the last element of the array is 30. It also reduces the length property of the myArray to 2.
## 2-Using an empty array with the pop() method
```javascript
const emptyArray = [];
const removedFromEmptyt = emptyArray.pop();

console.log(removedFromEmpty);  //Undefined
console.log(removedFromEmpty.length);  //0
```
Output:
```
Undefined
0
```
-We start with the myArray, which initially has 3 elements. When we use pop(), it removes the last element (30), and the array's length property is updated to 2.

-Next, we create an emptyArray that doesn't contain any elements. When we use pop() on this empty array, it returns undefined, and the length of the empty array remains 0.
## 3-Using JavaScript pop() method with array-like objects
```javascript
let greetings = {
  0: 'Hi',
  1: 'Hello',
  2: 'Howdy',
  length: 2,
  removeLast() {
    return [].pop.call(this);
  },
};

let greting = greetings.removeLast();

console.log(greting);
console.log(greetings);
```
Output:
```
'Howdy'

{
  '0': 'Hi',
  '1': 'Hello',
  length: 2,
  removeLast: [Function: removeLast]
}
```
In this example, we create an object named greetings. This object has elements with indexes such as 0, 1 and 2 and a length property. A method called removeLast() is also defined, and since this method operates on an array-like object, it calls the pop() method on that object using [].pop.call(this).

As a result, the last element from the greetings object is removed and this element is assigned to the variable greetings. Additionally, changes are made to the greetings object and you can view the results with console.log().

This example shows an example of using the pop() method with array-like objects. With this method, you can remove the last elements from array-like objects.

## Summary
-Use the pop() method to remove the last element of an array.

-Use the call() or apply() to call the pop() method on an array-like object.


