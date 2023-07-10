
# Day1 : Introduction , DOM , Values & Data Types , Operators1️⃣
This file summarizes the JavaScript lesson on Basic Javascript.These Consepts are important in programming for efficient code, string manipulation, and accessing specific characters in a string respectively. 
# Content
1. Principles of JavaScript
2. Callbacks & Higher order functions

## Lesson Summary:
In this lesson, we explored the hard part of JavaScript. Here are the key points covered:

* Execution Context: there's two part to executing code (thread of execution, Memory).
* Higher-order functions: Takes in a function or passes out a function.
* Map, filter, reduce - the most readable way to write code to work with data.  

   
## Coding Examples
```jsx
     //Example 1: Functions & Callbacks
     const num = 3;
  function multiplyBy2 (inputNumber){
  const result = inputNumber*2;
  return result;
  }
  const output = multiplyBy2(num);
  const newOutput = multiplyBy2(10);


     //Example 2: declare normal function vs. arrow function 
       function multiplyBy2(input) { return input * 2; }
       const multiplyBy2 = input => input *2;
       const output = multiplyBy2(3) //6

     //Example 3: Use Bracket Notation to Find the Nth-to-Last Character in a String
     const firstName = "Augusta";
     const thirdToLastLetter = firstName[firstName.length - 3];
```
## Coding Exercies
  **My Solution**   

[Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)

```jsx
      //Example 1: map, filter, and reduce
    const squareList = arr => {
   // Only change code below this line
    return arr
    .filter(num => Number.isInteger(num) && num > 0)
    .map(num => num ** 2);
  // Only change code above this line
  };
```
[Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)
```jsx
       //Example 2:  Convert Strings to URL Slugs

        const title = 'Winter Is Coming';
     function urlSlug(title) {
    return title
    .toLowerCase()
    .trim()
    .split(/\s+/)
    .join("-");
   }

```
[Question 1 & 2:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day1-tasks/tasks.md)
```jsx
     //Example 1: Functions & Callback
         const array = [1, 2, 3, 4, 5];

      function asyncMultiplyByTwo(value) {
     return new Promise((resolve) => {
    setTimeout(() => {
      resolve(value * 2);
       }, 1000);
     });
   }

   mapAsync(array, asyncMultiplyByTwo)
     .then((result) => {
       console.log(result); // [2, 4, 6, 8, 10]
     })
  .catch((error) => {
    console.error(error);
    });

    //Example 2 : Call Stack and Recursion
      const sumRange=(_start,_end)=>{
    if(_end>_start){
    return 0;
     }else{
    return _start + sumRange(_start +1 , _end);
    }
   }


```

