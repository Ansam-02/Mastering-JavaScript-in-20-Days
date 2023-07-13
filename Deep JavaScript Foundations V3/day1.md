
# Day1 : Introduction ,Types and Coercion
This file summarizes the JavaScript lesson on `Types` and `Coercion`.These Consepts are important in programming. the types are what determine the amount of memory allocated to save a value.`Coercion` is the process of converting a value from one data type to another. 

## Lesson Summary:
In this lesson, we explored the hard part of JavaScript. Here are the key points covered:

* Use the typeof operator to get the type of an object or variable in JavaScript.
* Primitive types are immutable and don't have properties.
* Non-primitive types can be used to call methods to perform certain operations.
* JavaScript variables can be converted to a new variable and another data type.
* Coercion With the Equality (==)/(===) Operators.
* JavaScript using built-in functions such as Number(), String(), Boolean(), parseInt(), and parseFloat(). 

   
## Coding Examples
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
  **My Solution**   

[Question 1](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

```jsx
      function convertStringToNumber(input) {
      return typeof input === 'string' ? +input || { value: input, type: 'Invalid Number' } : { value: input, type: typeof input };
      }
      console.log(convertStringToNumber("10"));
```
[Question 2](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

```jsx
    const checkNaN = (value) => {
    return isNaN(value);
   };

   console.log(checkNaN("4")); //returns false
```
[Question 3](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

```jsx
    function isEmptyValue(value) {
  return value === undefined || value === null || value === '';
  }
  console(isEmptyValue(0));  // Output: false
 


```
[Question 4](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

```jsx
    function compareObjects(input1, input2) {
  if (typeof input1 !== 'object' || typeof input2 !== 'object') {
    return [input1, input2];
  }
  
    return JSON.stringify(input1) === JSON.stringify(input2);
  }


```

[Question 5](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day1-tasks/tasks.md)

```jsx
    const complexCoercion = (input) => {
  if (typeof input !== 'object') {
    if (typeof input === 'number') {
      return Boolean(String(input));
    } else if (typeof input === 'string') {
      return Boolean(input);
    } else if (input === null || input === undefined) {
      return false;
    }
  }

    return input;
  };


```


