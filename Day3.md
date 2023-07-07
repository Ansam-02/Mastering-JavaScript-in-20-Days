# Day 3: Javascript Function
This file is about Function, Functions in JavaScript (JS) are reusable blocks of code that perform specific tasks when called, allowing for modularity and code organization. They can accept input parameters and return output values, enabling the creation of dynamic and interactive web applications. Understanding functions is crucial for efficient JS programming and building robust software solutions.

## Lesson Summary:
In this lesson, we explored the Functions in Javascript . Here are the key points covered:

* We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.
*  cope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope.
* Variables which are declared within a function, as well as the function parameters, have local scope.
* In Computer Science a queue is an abstract Data Structure where items are kept in order.
* items can be added at the back of the queue and old items are taken off from the front of the queue.

## Coding Examples
```jsx
     //Example 1: Return a Value from a Function with Return
     function plusThree(num) {
     return num + 3;
    }
     const answer = plusThree(5);


     //Example 2: Local Scope and Functions
     function myTest() {
      const loc = "foo";
     console.log(loc);
      }
      myTest();
        console.log(loc);


     //Example 3: Global vs. Local Scope in Functions
      const someVar = "Hat";
      function myFun() {
      const someVar = "Head";
      return someVar;
      }
```
## Coding Exercies
  **My Solution**   

[Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)

```jsx
        function timesFive(num) {
        return num * 5;
    }
```
[Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)
```jsx
       //Example 2: Global Scope and Functions
       var num1 = 18; // Global scope
    function fun() {
   var num2 = 20; // Local (Function) Scope
   if (true) {
    var num3 = 22; // Block Scope (within an if-statement)
   }
  }

```
[Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)
```jsx
      //Example 3: Local Scope and Functions
     function spreadOut() {
     let fragment = ["to", "code"];
     let sentence = ["learning", ...fragment, "is", "fun"]; // change this line
     return sentence;
      }

      // do not change code below this line
   console.log(spreadOut());
```
[Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)
```jsx
      //Example 4: Global vs. Local Scope in Functions
     var outerWear = "T-Shirt";

    function myOutfit() {
    var outerWear = "sweater";
     return outerWear;
    }
   myOutfit();
```
[Stand in Line]()
```jsx
      //Example 5: Stand in Line
     function nextInLine(arr, item) {
   // Only change code below this line
   arr.push(item);
   const removed = arr.shift();
   return removed;
   // Only change code above this line
   }
```
