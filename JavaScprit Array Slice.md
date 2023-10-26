# Introduction to JavaScript Array slice() method
`slice(start, stop);`

1.The **start** parameter determines the zero-based index of the array to start extracting. If start is not specified, slice() subtracts from the beginning of the array.

2.The **stop** parameter determines the index at which the extraction process will end. The slice() method does not include the index specified by the end parameter in the new array. If no end is specified, slice() uses the length of the array as the end.

`Note:` The slice() method returns a new array and only superficially copies the elements of the array. It does not modify the source array.
## 1-Cloning an array
```javascript
var numbers = [1, 2, 3, 4, 5];
var newNumbers = numbers.slice();
```
In this example, the newNumbers array contains all the elements of the numbers array. The two series are independent of each other.
## 2- Copy a portion of an array
```javascript
var colors = ['red', 'green', 'blue', 'yellow', 'purple']
var rgb = colors.slice(0, 3);
```
The rgb array contains the first three elements of the colors array. 

`Warning!` The source array colors are not changed.

## 3-Convert array-like objects into arrays
```javascript
function toArray() {
  return Array.prototype.slice.call(arguments);
}

var classification = toArray('A', 'B', 'C');
console.log(classification); // ["A", "B", "C"]
```
1.First, we define a function called toArray. This function will convert all arguments passed to it into an array.

2.Using the Array.prototype.slice call, we convert the arguments object passed to the function itself into an array. The slice method is widely used to convert an array-like object into an actual array. The call method allows us to call the slice method on the arguments object.

3.The result of the toArray operation is assigned to the classification variable. So classification becomes an actual array containing 'A', 'B' and 'C'.

4.Finally, console.log(classification); Using this method, we print the classification array to the console and see ["A", "B", "C"] as output.

We can also select <p> (paragraph) elements in the HTML document and convert them into a JavaScript array:
```javascript
var p = document.querySelectorAll('p');
var list = Array.prototype.slice.call(p);
```
1.First, we select all <p> elements in the HTML document using document.querySelectorAll('p'). The querySelectorAll method returns a NodeList. NodeList is similar to an array, but it is not a real array.

2.Next, we use Array.prototype.slice.call(p) to convert this NodeList into an actual JavaScript array. This line performs the following operations:

  -We access the slice method of the Array object using Array.prototype.

  -With call(p) we call this method on the p (NodeList) object. Using call, the slice method operates on the object p and creates an actual array containing the elements of this object.

As a result, a new array named list will contain all < p > elements in the HTML document. This array can now use methods specific to arrays and unlike NodeList, you can easily operate on arrays. This is a common usage, especially when working with the DOM (Document Object Model), because the DOM usually returns a NodeList, and turning that NodeList into an actual array makes things easier.







