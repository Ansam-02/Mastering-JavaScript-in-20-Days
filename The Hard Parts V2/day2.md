# Day 2 : Closure (scope and execution context)
This file summarizes the JavaScript lesson on Closure (scope and execution context).These Consepts are important in programming for efficient code, Closure gives our functions persistent memories and
entirely new toolkit for writing professional code.

## Lesson Summary:
In this lesson, we explored the Closure. Here are the key points covered:
* JavaScript variables can belong to the local or global scope.
* Global variables can be made local (private) with closures.
* Variables created without a declaration keyword (var, let, or const) are always global, even if they are created inside a function.
* A closure is a function having access to the parent scope, even after the parent function has closed.
   
## Coding Examples
```jsx
     //Example 1: Functions get a new memory every run
     function multiplyBy2 (inputNumber){
const result = inputNumber*2;
return result;
}
const output = multiplyBy2(7);
const newOutput = multiplyBy2(10);

     //Example 2: Functions returned from other functions 
       function createFunction() {
   function multiplyBy2 (num){
   return num*2;
   }
   return multiplyBy2;
  }
  const generatedFunc = createFunction();
  const result = generatedFunc(3); // 6

     //Example 3: Calling a function outside of the function call in 
     function outer (){
   let counter = 0;
   function incrementCounter (){ counter ++; }
   return incrementCounter;
  }
  const myNewFunction = outer();
  myNewFunction();
  myNewFunction();
```
## Coding Exercies
  **My Solution**   


[Question 1:]([https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md))
```jsx
       

```
[Question 2:]([https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day1-tasks/tasks.md](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md))
```jsx
   


```
[Question 3:]([https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day1-tasks/tasks.md](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md))
```jsx

```

[Question 4:]([https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day1-tasks/tasks.md](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md))
```jsx

```
