# Introduction to JavaScript multidimensional array
Multidimensional arrays in JavaScript are arrays containing elements of more than one dimension. That is, within an array there are other arrays, and these nested arrays form a multidimensional structure. These multidimensional arrays can be structured like a table or matrix.

To declare an empty multidimensional array, you use the same syntax as declaring one-dimensional array:
```javascript
let activities = [];
```
The following example defines a two-dimensional array named activities:
```javascript
let activities = [
    ['Work', 9],
    ['Eat', 1],
    ['Commute', 2],
    ['Play Game', 1],
    ['Sleep', 7]
];
```
To show the activities array in the console, you use the console.table() method as follows:
```javascript
console.table(activities);
```
Output:

```
┌─────────┬─────────────┬───┐
│ (index) │      0      │ 1 │
├─────────┼─────────────┼───┤
│    0    │   'Work'    │ 9 │
│    1    │    'Eat'    │ 1 │
│    2    │  'Commute'  │ 2 │
│    3    │ 'Play Game' │ 1 │
│    4    │   'Sleep'   │ 7 │
└─────────┴─────────────┴───┘
```

To access an element of a multidimensional array
```javascript
console.log(activities[0][1]); // 9
```
## 1-Adding elements
You can use the Array methods such as push() and splice() to manipulate elements of a multidimensional array.
```javascript
activities.push(['Study',2]);

console.table(activities);
```
Output:

```
┌─────────┬─────────────┬───┐
│ (index) │      0      │ 1 │
├─────────┼─────────────┼───┤
│    0    │   'Work'    │ 9 │
│    1    │    'Eat'    │ 1 │
│    2    │  'Commute'  │ 2 │
│    3    │ 'Play Game' │ 1 │
│    4    │   'Sleep'   │ 7 │
│    5    │   'Study'   │ 2 │
└─────────┴─────────────┴───┘
```
```javascript
activities.splice(1, 0, ['Programming', 2]);

console.table(activities);
```
Output:

```
┌─────────┬───────────────┬───┐
│ (index) │       0       │ 1 │
├─────────┼───────────────┼───┤
│    0    │    'Work'     │ 9 │
│    1    │ 'Programming' │ 2 │
│    2    │     'Eat'     │ 1 │
│    3    │   'Commute'   │ 2 │
│    4    │  'Play Game'  │ 1 │
│    5    │    'Sleep'    │ 7 │
│    6    │    'Study'    │ 2 │
└─────────┴───────────────┴───┘
```
## 2-Adding column
```javascript
activities.forEach(activity => {
    let percentage = ((activity[1] / 24) * 100).toFixed();
    activity[2] = percentage + '%';
});

console.table(activities);
```
Output:

```
┌─────────┬───────────────┬───┬───────┐
│ (index) │       0       │ 1 │   2   │
├─────────┼───────────────┼───┼───────┤
│    0    │    'Work'     │ 9 │ '38%' │
│    1    │ 'Programming' │ 2 │ '8%'  │
│    2    │     'Eat'     │ 1 │ '4%'  │
│    3    │   'Commute'   │ 2 │ '8%'  │
│    4    │  'Play Game'  │ 1 │ '4%'  │
│    5    │    'Sleep'    │ 7 │ '29%' │
│    6    │    'Study'    │ 2 │ '8%'  │
└─────────┴───────────────┴───┴───────┘
```
## 2-Removing elements
```javascript
activities.pop();

console.table(activities);
```
Output:

```
┌─────────┬───────────────┬───┬───────┐
│ (index) │       0       │ 1 │   2   │
├─────────┼───────────────┼───┼───────┤
│    0    │    'Work'     │ 9 │ '38%' │
│    1    │ 'Programming' │ 2 │ '8%'  │
│    2    │     'Eat'     │ 1 │ '4%'  │
│    3    │   'Commute'   │ 2 │ '8%'  │
│    4    │  'Play Game'  │ 1 │ '4%'  │
│    5    │    'Sleep'    │ 7 │ '29%' │
└─────────┴───────────────┴───┴───────┘
```
## 2-Removing column
```javascript
activities.forEach((activity) => {
    activity.pop(2);
});

console.table(activities);
```
Output:

```
┌─────────┬───────────────┬───┐
│ (index) │       0       │ 1 │
├─────────┼───────────────┼───┤
│    0    │    'Work'     │ 9 │
│    1    │ 'Programming' │ 2 │
│    2    │     'Eat'     │ 1 │
│    3    │   'Commute'   │ 2 │
│    4    │  'Play Game'  │ 1 │
│    5    │    'Sleep'    │ 7 │
└─────────┴───────────────┴───┘
```
## 2-Iterating over elements
```javascript
// loop the outer array
for (let i = 0; i < activities.length; i++) {
    // get the size of the inner array
    var innerArrayLength = activities[i].length;
    // loop the inner array
    for (let j = 0; j < innerArrayLength; j++) {
        console.log('[' + i + ',' + j + '] = ' + activities[i][j]);
    }
}
```
Output:

```
[0,0] = Work
[0,1] = 9
[1,0] = Eat
[1,1] = 1
[2,0] = Commute
[2,1] = 2
[3,0] = Play Game
[3,1] = 1
[4,0] = Sleep
[4,1] = 7
[5,0] = Study
[5,1] = 2
```
Or you can use the forEach() method twice:
```javascript
activities.forEach((activity) => {
    activity.forEach((data) => {
        console.log(data);
    });
});
```
Output:

```
Work
9
Eat
1
Commute
2
Play Game
1
Sleep
7
Study
2
```



