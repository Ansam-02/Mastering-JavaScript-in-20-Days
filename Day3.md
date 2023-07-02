# What I learned from the third day tasks
### This Section focus on Function 
## Examples:
1. Return a Value from a Function with Return,
and here is my solution for the task:
```javascript

 function timesFive(num){
  return num * 5;
}
```
2. Global Scope and Functions
  ```javascript

   // Declare the myGlobal variable below this line
let myGlobal = 10;

function fun1() {
  // Assign 5 to oopsGlobal here
  oopsGlobal = 5;
}
```

3. Local Scope and Functions
```javascript
 function myLocalScope() {

  // Only change code below this line
  var myVar;
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

```
4. Global vs. Local Scope in Functions

  ```javascript
function myOutfit() {
  // Only change code below this line
  var outerWear = 'sweater';
  // Only change code above this line
  return outerWear;
}

myOutfit();
 ```
5. Stand in Line

```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  let removeditem = arr.shift();
  return removeditem;
  return item;
  // Only change code above this line
}
```

   



