# Day 2 : Closure (scope and execution context)
This file summarizes the JavaScript lesson on Closure (scope and execution context).These Consepts are important in programming for efficient code, Closure gives our functions persistent memories and
entirely new toolkit for writing professional code.

## Lesson Summary:
In this lesson, we explored the Closure. Here are the key points covered:
* What is closure in Javascript.
* How to use it. 
* talk about Variables created without a declaration keyword (var, let, or const).
* Calling multi functions.
   
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


[Question 1:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md)
```jsx
   function createCounter (start){
   let counter = start;
   const inc_fun = ()=>{
       return counter++;
   };
   return inc_fun;
   };
   const result = createCounter(0);
   console.log(result());    

```
[Question 2:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md)
```jsx
         const calculateAverage =(arr)=>{
    const calsum=()=>{
     let sum = 0;
     for(let i = 0; i < arr.length ; i++){
         sum+=arr[i];
     }
     return sum/arr.length;
    };

    return calsum;

   };
   const fun = calculateAverage([2,4,6,8,10]);
   console.log(fun());

```
[Question 3:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day2-tasks/tasks.md)
```jsx
         const powerOf =(base) =>{
    const expfun = (exp)=>{
        return base ** exp;
          
        };
        return expfun;
       };
   const fun = powerOf(2);
   console.log(fun(6));
```

[Question 4:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week2-day1-tasks/tasks.md)
```jsx
      const compose = (...fns) => {
       return (arg) => {
       let result = arg;
       for (let i = fns.length - 1; i >= 0; i--) {
      result = fns[i](result);
    }
    return result;
     };
   };

   const myFunComposed = compose(
     (x) => x / 10,
     (x) => x / 5,
     (x) => x - 50
   );

      console.log(myFunComposed(100)); 
     // Output: 1
```
