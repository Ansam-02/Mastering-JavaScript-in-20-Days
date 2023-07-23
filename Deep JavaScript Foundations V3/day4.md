
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
      
```
## [Question 3](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      
```
## CLOSURE:
## [Question 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      
```
## [Question 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

```jsx
      
```
