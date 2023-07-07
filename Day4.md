# Day 4: Javascript Algorithm Using Method
Map, filter, and ternary operators are powerful tools in JavaScript for manipulating data and making conditional decisions.


## Lesson Summary:
In this lesson, we explored the Basic JavaScript. Here are the key points covered:
* The map function allows us to transform elements of an array by applying a specified function to each element and returning a new array with the transformed values.
* Filter, on the other hand, enables us to selectively extract elements from an array based on a given condition, creating a new array with only the matching elements.
* The ternary operator provides a concise way to write conditional statements in a single line, making it easy to assign values or execute code based on a condition.
   
## Coding Examples
```jsx
     //Example1: Use Multiple Conditional (Ternary) Operators
     function findGreaterOrEqual(a, b) {
     return (a === b) ? "a and b are equal" 
    : (a > b) ? "a is greater" 
    : "b is greater";
         }


     //Example 2: Golf Code
     let ourStr = "I come first. ";
     ourStr += "I come second.";
     
     //Example 3: Use the map Method to Extract Data from an Array
        const users = [
     { name: 'John', age: 34 },
     { name: 'Amy', age: 20 },
     { name: 'camperCat', age: 10 }
      ];

         const names = users.map(user => user.name);
         console.log(names);


        //Example 4: Use the filter Method to Extract Data from an Array
               const users = [
           { name: 'John', age: 34 },
           { name: 'Amy', age: 20 },
           { name: 'camperCat', age: 10 }
      ];

     const usersUnder30 = users.filter(user => user.age < 30);
     console.log(usersUnder30); 

```
## Coding Exercies
  **My Solution**   

[Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)

```jsx
      //Example 1:Use Multiple Conditional (Ternary) Operators
   function checkSign(num) {
  return num > 0 ? "positive"
    : num < 0 ? "negative"
    : "zero";
  }
     
```
[Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)
```jsx
       //Example 2: Golf Code
             const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

      function golfScore(par, strokes) {
     return strokes === 1
    ? names[0]
    : strokes <= par - 2
    ? names[1]
    : strokes === par - 1
    ? names[2]
    : strokes === par
    ? names[3]
    : strokes === par + 1
    ? names[4]
    : strokes === par + 2
    ? names[5]
    : names[6];
   }
```
[Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)
```jsx
      //Example 3: Use the map Method to Extract Data from an Array
      const ratings = watchList.map(({ Title: title, imdbRating: rating }) => ({title, rating}));
     
```
[Use the Filter Method to Extract Data from an Array](https://forum.freecodecamp.org/t/freecodecamp-challenge-guide-use-the-filter-method-to-extract-data-from-an-array/18179)
```jsx
      //Example 4: Use the Filter Method to Extract Data from an Array
      const filteredList = watchList
  .filter(movie => movie.imdbRating >= 8.0)
  .map(movie => ({ title: movie["Title"], rating: movie["imdbRating"] }));
   // Only change code above this line
   console.log(filteredList);
     
```
