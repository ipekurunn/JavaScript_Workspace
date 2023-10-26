# JavaScript array indexOf() method
The `indexOf()` method is used to find the position of a particular element in an array. Returns the index of the first found position of the searched element in the array. If the element is not found, it returns -1.
`Array.indexOf(searchElement, fromIndex)`
1.The searchElement argument represents the element you want to search in the array.

2.fromIndex specifies the index value from which the search process will start. This parameter is optional. If not specified, the search starts from the beginning of the array.

3.fromIndex can be a negative integer, and if it is negative, the indexOf() method starts the search from the end of the array.
```javascript
var scores = [10, 20, 30, 10, 40, 20];

console.log(scores.indexOf(10)); // 0
console.log(scores.indexOf(30)); // 2
console.log(scores.indexOf(50)); // -1
console.log(scores.indexOf(20)); // 1
```
**Usage of negative fromIndex:**
```javascript
var scores = [10, 20, 30, 10, 40, 20];

console.log(scores.indexOf(20,-1)); // 5 (fromIndex = 6+ (-1) = 5)
console.log(scores.indexOf(20,-5)); // 1 (fromIndex = 6+ (-5) = 1)
```
**Usage with objects in an array**
```javascript
var guests = [
    {name: 'John Doe', age: 30},
    {name: 'Lily Bush', age: 20},
    {name: 'William Gate', age: 25}
];
```
This piece of code represents three objects in a JavaScript array guests. Each object has two properties: name and age. These objects store people's names and ages.

The array contains multiple objects within {} curly braces. Each object is specified with two keywords (properties):

By hiding these objects, the series keeps the names and ages of different people together. For example, guests[0] represents the first person ({name: 'John Doe', age: 30}). This array is used to store and access data in an organized manner.
```javascript
console.log(guests.indexOf({
    name: 'John Doe',
    age: 30
})); // -1
```
When comparing objects, the indexOf() method checks their contents, not their references.
Although the {name: 'John Doe', age: 30} object in the guests array and the {name: 'John Doe', age: 30} object that is tried to be searched with indexOf() have the same content, they have different references. Therefore indexOf() cannot find this object in the array and returns -1.

**Finding the indexes of all formations of an element in a array**
```javascript
function find(needle, haystack) {
    var results = [];  // Creating an array to store the results.
    var idx = haystack.indexOf(needle);  // Finds the index of the first element.
    while (idx != -1) {
        // Adds the index of the first element found to the results array.
        results.push(idx);
        //Updating the index for the next search.
        idx = haystack.indexOf(needle, idx + 1);
    }
    return results;
}
```
1. **needle:** The item you are looking for.
2. **haystack:** The array you want to search.
```javascript
var scores = [10, 20, 30, 10, 40, 20];
console.log(find(10, scores)); // [0, 3]
```
# JavaScript array lastIndexOf() method
The lastIndexOf() method returns the index of the last occurrence of a given element in an array. If it cannot find the element, it returns -1.

`Array.lastIndexOf(searchElement[, fromIndex = Array.length - 1])`

1.**searchElement** represents the element searched in the array.

2.**fromIndex** specifies from which index location the search will start. This parameter is optional. If not specified, the search *starts from the end* of the array.

```javascript
var scores = [10, 20, 30, 10, 40, 20];

console.log(scores.lastIndexOf(10)); // 3
console.log(scores.lastIndexOf(20)); // 5
console.log(scores.lastIndexOf(50)); // -1
```
