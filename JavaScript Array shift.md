# Introduction to the JavaScript Array shift() function
`array.shift()`
The shift() method is used to remove the first element from an array.
## 1-Removing the first element from an array
```javascript
const numbers = [10, 20, 30];
let removingNumber = numbers.shift();

console.log({ removingNumber });
console.log({ numbers });
console.log({ length: numbers.length });
```
Output:
```
{ number: 10 }
{ numbers: [ 20, 30 ] }
{ length: 2 }
```
## 2-Removing all first element from an array
```javascript
const numbers = [10, 20, 30]
let removingNumber;
while ((number == numbers.shift()) != undefined) {
  console.log(removingNumber);
}
```
Output:
```
10
20
30
```
## 3-Using the JavaScript array shift() with array-like object
```javascript
let greetings = {
  0: 'Hi',
  1: 'Hello',
  2: 'Howdy',
  length: 3,
  removeFirst() {
    return [].shift.call(this);
  },
};

const greeting = greetings.removeFirst();

console.log(greeting);
console.log(greetings);
```
In this example, we created an object named greetings. This object resembles an array because it has indexes starting from zero and a length property.

1.We defined a method called removeFirst(). This method is used to call the shift() method. However, the shift() method does not work directly on the greetings object, because the shift() method can only be used on arrays. Therefore, the shift() method is called with this using shift.call(this). this represents the greetings object.

2.We then call the removeFirst() method using the greetings.removeFirst() call. This uses the shift() method to remove the first element from the array.

3.We assign the first removed element to the greeting variable.

4.Finally, we print the greeting variable and greetings object to the console.
Output:
```
Hi
{
  0: 'Hello',
  1: 'Howdy',
  length: 2,
  removeFirst: [Function: removeFirst]
}
```
As you can see, the removeFirst() method removes the first element of the greetings object using the shift() method. The length property of the greetings object is reduced and other indexes are edited. Therefore Hi is removed, index 0 now contains Hello and index 1 contains Howdy.
