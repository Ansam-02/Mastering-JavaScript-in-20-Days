# Day 1: Expressions, Arrays and Objects
This file is about fundamental data structures in programming. Arrays allow us to store and access multiple values of the same type, while objects enable us to group related data and functionality together. Expressions, on the other hand, are combinations of values, variables, and operators that evaluate to a result. They are the building blocks of logic and computation in programming languages. Understanding these concepts is crucial for effectively manipulating data and performing complex operations in programming.

## Lesson Summary:
In this lesson, we explored the Basic JavaScript and Data Structure. Here are the key points covered:

* We have an array of objects representing different people in our contacts lists.
*  The slice() method returns a shallow copy of a portion of an array into a new array object selected from start to end
* Combine Arrays with the Spread Operator: create a new array and then spread the values of array1 followed by array2 in it.
   
## Coding Examples
```jsx
     //Example 1: Copy Array Items Using slice()
     let weatherConditions = ['rain', 'snow', 'sleet', 'hail', 'clear'];
      let todaysWeather = weatherConditions.slice(1, 3);

     //Example 2: Combine Arrays with the Spread Operator
      let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];
      let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
     
```
## Coding Exercies
  **My Solution**   

[Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

```jsx
      //Example 1: Profile lookup
     function lookUpProfile(name, prop) {
  for (let x = 0; x < contacts.length; x++) {
    if (contacts[x].firstName === name) {
      if (contacts[x].hasOwnProperty(prop)) {
        return contacts[x][prop];
      } else {
        return "No such property";
       }
     }
   }
  return "No such contact";
 }
```
[Copy Array Items Using slice](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)
```jsx
       //Example 2: Copy Array Items Using slice
          function forecast(arr) {
     // change code below this line
     return arr.slice(2, 4);
     }

   // do not change code below this line
      console.log(
     forecast(["cold", "rainy", "warm", "sunny", "cool", "thunderstorms"])
   );
```
[Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)
```jsx
      //Example 3: Combine Arrays with the Spread Operator
     function spreadOut() {
     let fragment = ["to", "code"];
     let sentence = ["learning", ...fragment, "is", "fun"]; // change this line
     return sentence;
      }

      // do not change code below this line
   console.log(spreadOut());
```
