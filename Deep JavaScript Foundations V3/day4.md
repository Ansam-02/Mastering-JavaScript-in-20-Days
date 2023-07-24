
# Day4 : Advanced Scope and Closure
This file summarizes the JavaScript lesson on `Types` and `Coercion`.These Consepts are important in programming. the types are what determine the amount of memory allocated to save a value.`Coercion` is the process of converting a value from one data type to another. 

## Lesson Summary:
In this lesson, we explored the hard part of JavaScript, The Advanced Scope and Closure. Here are the key points covered:

* Lexical scope describes how nested (also known as "child") functions have access to variables defined in parent scopes.here is an example:
```jsx
  const myFunction = () => {
     let myValue = 2;
     console.log(myValue);

     const childFunction = () => {
          console.log(myValue += 1);
     }

     childFunction();
}

myFunction();
```
* A closure is a function having access to the parent scope, even after the parent function has closed.
* IIFE (Immediately Invokable Function Expression) is a important concept in JavaScript. it is a commonly used Design Pattern which is used to wrap set of variables and functions which cannot be accessed outside the enclosed scope.
* Hoisting is JavaScript's default behavior of moving declarations to the top.
* strict mode does not allow variables to be used if they are not declared.
  

  **My Solution**   
## ADVANCED SCOPE:
## [Question 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

To fix this and achieve the desired output, we need to capture the current value of i at each iteration and create a new scope to maintain the correct value for each iteration. We can do this by using an Immediately Invoked Function Expression (IIFE) inside the loop.

Here's the modified code to fix the issue:
```jsx
      for (var i = 0; i < 5; i++) {
  (function (index) {
    setTimeout(function () {
      console.log("value of [i] is: ", index);
    }, 100);
  })(i);
}

```
here is the result of the code:   
`"value of [i] is: 0"`  
`"value of [i] is: 1"`  
`"value of [i] is: 2"`  
`"value of [i] is: 3"`  
`"value of [i] is: 4"`  

## [Question 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
     let array = []; // Move the array declaration outside of the loop

 for (let i = 0; i < 5; i++) {
   array.push(i);
   console.log("Current array is: ", array);
 }
 
```
To fix this and achieve the desired output of a single array containing all the values from 0 to 4, we need to move the array declaration outside of the loop. This way, the array will not be reinitialized in each iteration, and all the values of i will be pushed into the same array.  
here is the output:  
`"Current array is: [0]"`  
`"Current array is: [0, 1]"`  
`"Current array is: [0, 1, 2]"`  
`"Current array is: [0, 1, 2, 3]"`  
`"Current array is: [0, 1, 2, 3, 4]"`  

## [Question 3](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      let functions = [];

for (let i = 0; i < 5; i++) { // Use let instead of var for i
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```
To fix this and achieve the desired output, we can use the `let` keyword instead of var to declare the loop variable i. This way, each iteration will have its own separate lexical environment and a unique i value will be captured by each arrow function.


## CLOSURE:
## [Question 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      function privateCounter() {
  let count = 0;

  function increment() {
    count++;
  }

  function getCount() {
    return count;
  }

  return {
    increment: increment,
    getCount: getCount
  };
}

// Example usage:

const counter1 = privateCounter();
const counter2 = privateCounter();

counter1.increment();
counter1.increment();
console.log(counter1.getCount()); // Output: 2

counter2.increment();
console.log(counter2.getCount()); // Output: 1

```
## [Question 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      function generateFibonacci(count) {
  let currentCount = 0;
  let prev1 = 0;
  let prev2 = 1;

  function fibonacci() {
    if (currentCount === 0) {
      currentCount++;
      return prev1;
    } else if (currentCount === 1) {
      currentCount++;
      return prev2;
    } else {
      const nextFib = prev1 + prev2;
      prev1 = prev2;
      prev2 = nextFib;
      currentCount++;

      if (currentCount <= count) {
        return nextFib;
      } else {
        return undefined;
      }
    }
  }

  return fibonacci;
}

```
