
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

```jsx
     
```
  

