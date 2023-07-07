# Day 1: Introduction to DOM & Data Types
This README file summarizes the JavaScript lesson on Basic Javascript.These Consepts are important in programming for efficient code, string manipulation, and accessing specific characters in a string respectively.

## Lesson Summary:
In this lesson, we explored the Basic JavaScript. Here are the key points covered:
* compound Assignment With Augmented Multiplication

     num*=2 which is the same of num = num*2
   
 Concatenating Strings with the Plus Equals Operator
   ```javascript
     let NAME = "My Name is ";
      NAME += "Ansam";
   ```
4) Use Bracket Notation to Find the Nth-to-Last Character in a String
   ```javascript
     const firstName = "Ansam";
     const theletter = firstName[firstName.length - 2]; //the result=a
   ```
## Coding Examples
```jsx
     //Example 1: compound Assignment
     myVar = myVar * 5;

     //Example 2: Concatenating Strings '+='
     let ourStr = "I come first. ";
     ourStr += "I come second.";
     
     //Example 3: Use Bracket Notation to Find the Nth-to-Last Character in a String
     const firstName = "Augusta";
     const thirdToLastLetter = firstName[firstName.length - 3];
```
## Coding Exercies
[https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication]
**My Solution**
```jsx
      //Example 1: compound Assignment
     var c = 2;
     c *= 3; // Now, 'c' is equal to 6
```
[https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator]
```jsx
       //Example 2: Concatenating Strings '+='
          let str = "Hello ";
     str += "coding"; // Now the string reads "Hello coding"
     str += "camper!"; // And now the string reads "Hello codingcamper!"
```
[https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string]
```jsx
      //Example 3: Use Bracket Notation to Find the Nth-to-Last Character in a String
     var str = "Programming";
     var secondToLastChar = str[str.length - 2]; // This is 'i'
```
