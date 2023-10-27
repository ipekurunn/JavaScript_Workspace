
The concat() method creates a new array by concatenating one or more arrays and does not modify the original arrays.
```javascript
let odds = [1, 3, 5];
let evens = [2, 4, 6];
let combined = odds.concat(evens);

console.log('Result:', combined);
console.log('Odds:', odds);
```
Output:

`Result: [1, 3, 5, 2, 4, 6]
Odds: [1, 3, 5]
`
## 1-Usage with empty array
```javascript
let odds = [1, 3, 5];
let evens = [2, 4, 6];
let combined = [].concat(odds, evens);

console.log(combined);
```
Output:

`Odds: [1, 3, 5]`

## 2-Merge multiple arrays
```javascript
let upper = ['A', 'B', 'C'];
let lower = ['a', 'b', 'c'];
let digits = [1, 2, 3];
let alphanumerics = upper.concat(lower, digits);

console.log(alphanumerics);
```
Output:

`['A', 'B', 'C', 'a', 'b', 'c', 1, 2, 3]`

## 3-Don’t pass any argument into the concat() method
```javascript
let colors = ['red', 'green', 'blue'];
let rgb = colors.concat();

console.log(rgb);
```
Output:

`['red', 'green', 'blue']`

## 4-Pass values that are not arrays
```javascript
let rgb = ['red', 'green', 'blue'];
let moreColors = rgb.concat('yellow', 'magenta'); // They are not in any array.

console.log(moreColors);
```
Output:

`['red', 'green', 'blue', 'yellow', 'magenta']`

## 5-Spread Operator
```javascript
let odds = [1, 3, 5];
let evens = [2, 4, 6];
let combined = [...odds, ...evens];

console.log(combined);
```
Output:

`[1, 3, 5, 2, 4, 6]`



