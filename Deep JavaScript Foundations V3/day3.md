
# Day1 : Scope and Function Expressions
This file summarizes the JavaScript lesson on `scope of the function`.These Consepts are important in programming. When a variable is declared inside a function, it is only accessible within that function and cannot be used outside that function. 

## Lesson Summary:
In this lesson, we explored the scope of the function hard part of JavaScript. Here are the key points covered:
* JavaScript has the following two distinct types of scope:
    1.Function scope
    2.Block scope
* Function scope in JavaScript is created inside functions. When a function is declared.here is an examole:
 ```jsx
      var example = 5;
 function test() {
  var testVariable = 10;
  console.log( example ); // Expect output: 5
  console.log( testVariable ); // Expect output: 10
 }
 test();
 console.log( testVariable ); // Expect reference error
```
* Function Scope Hoisting,it's declaration automatically gets hoisted to the top of the scope. Hoisting means that the interpreter moves the instantiation of an entity to the top of the scope it was declared in, here is an example
  ```jsx
   example = 5; // Assign value
   console.log( example ); // Expect output: 5
   var example; // Declare variable

  ```
  * Block Scope, A new block scope in JavaScript is created with curly braces ({}). A pair of curly braces can be placed anywhere in the code to define a new scope block.
    ```jsx
    // Top level scope
function scopeExample() {
  // Scope block 1
  for ( let i = 0; i < 10; i++ ){ /* Scope block 2 */ }
  if ( true ) { /* Scope block 3 */ } else {  /* Scope block 4 */ }
  // Braces without keywords create scope blocks
  { /* Scope block 5 */ } 
  // Scope block 1
}
// Top level scope
    ```


```jsx
     //Example 1: Primitive Data
    typeof "John"              // Returns "string"
    typeof 3.14                // Returns "number"
    typeof true                // Returns "boolean"
    typeof false               // Returns "boolean"
    typeof x                   // Returns "undefined" (if x has no value)


     //Example 2: JavaScript Type Conversion
        String(x)         // returns a string from a number variable x
        d = new Date();
         Number(d)          // returns 1404568027739
        String(false)      // returns "false"
        Number(false)     // returns 0

     //Example 3 : Coercion
    
```
## Coding Exercies
### Scope & Function Expressions:  

## [Question 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day3-tasks/tasks.md)

```jsx
     
const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
}

const exampleNormalFunc2 = (x, y) => {
  return x * y;
}

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
}


const arrowHOF = (normalFunc) => {
  //here is my solution:
  const arrowHOF = (normalFunc) => {
  return (...args) => {
    return (...multiplierArgs) => {
      let result = normalFunc(...args);
      const numberOfTimes = multiplierArgs[0] || 1;

      for (let i = 0; i < numberOfTimes - 1; i++) {
        result = normalFunc(...args);
      }

      return result;
    };
  };
};

}

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1);
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3);

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 60 twice
console.log(hofNormalFunc2(20, 35))(4); // logs 700 four times
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once

```

## [Question 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day3-tasks/tasks.md)

```jsx
     
// Example object
const obj = {
  name: 'John',
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}!`);
  }
};

const preserveThis = (func) => {
  // write your code here;
  const preserveThis = (func) => {
  return (...args) => {
    return func.apply(func, args);
  };
};

  return func;
}

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet('Hello'); // Output: "Hello, John!"

```
## [Question 3](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day3-tasks/tasks.md)

Consider the 2 following examples and distinguish the different output in each one with them with a reasoning.

Example 1:
```jsx
function outer1() {
  var x = 10;

  var inner1 = function() {
    console.log(x);
  };

  inner1();
}

outer1(); // Output: 10
```
Reasoning for example 1's output: because x decalred by var which has a function scope ,so the output = 10, even if declared outside the blocked scope.

Example 2:
```jsx
function outer2() {
  var x = 10;

  var inner2 = function() {
    var x = 20;
    console.log(x);
  };

  inner2();
}

outer2(); // Output: 20
```
Reasoning for example 2's output: function inner2 has its own x variable, which shadows the outer x variable. This leads to different outputs when the inner functions are executed.

