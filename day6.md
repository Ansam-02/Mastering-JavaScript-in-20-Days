# Day 6 : Introduction to Map,Filter ,Promises ,API ,and Destructuring Data 
  It includes Topic of  `Map`, `Filter`, `Promises`, and `Destructuring` are essential concepts in JavaScript.   , returning a new array with the transformed values.

  
# Lesson Summary
- setTimeout() method sets a timer which executes a function or specified piece of code once the timer expires.
- Map is a function that takes an array and applies a transformation to each element.
- Filter ceates a new array by selectively including elements from an existing array based on a specified condition.
- Promises are objects used to handle asynchronous operations, allowing us to manage the completion or failure of tasks.
- API are constructs made available in programming languages to allow developers to create complex functionality more easily Finally.
- Destructuring provides a concise syntax for extracting values from objects or arrays, making it easier to access and work with specific elements of complex data structures.
- json() is async fun.
- URLs the way that we got data from the Internet.


```jsx
      //example1 create a new array with only the names of the girls
      const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
            ];
    const names = spices.map(s=> spices.name);

     //example2 create a new array endINY with the girls whose nicknames end with 'y'
    const endINY = spices.filter(s=>s.nickname[s.nicknames.length-1 ]=== 'y');

       //Example3 on setTimeout():
            setTimeout(() => {
            console.log("Delayed for 1 second.");
              }, "1000");

      //example4 await
      let response = await fetch("https://dog.ceo/api/breed/hound/list");
     console.log(response);

      //example Destruturing
      const spices = [{name:"Sarah", nickname:"queen"}]
        let {name, nickname} = spices[0];

        //example Debbugging
      function whyIsntThisWorking(input) {
        console.log("Well at least we got this far");
        console.log(input);
        return thingThatDoesntWork(input);
        }
      
```



# Coding Exercies for the Topics
1. `Map exercies`
```jsx
    const array1 = [1, 4, 9, 16];
   // Pass a function to map
   const map1 = array1.map(x => x * 2);
    console.log(map1);
    // Expected output: Array [2, 8, 18, 32]

```
2. `filter exercies`
```jsx
    const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
    const result = words.filter(word => word.length > 6);
    console.log(result);
    // Expected output: Array ["exuberant", "destruction", "present"]
```
3. `Promise's exercies`
```jsx
     const promiseA = new Promise((resolve, reject) => {
  resolve(777);
     });
    // At this point, "promiseA" is already settled.
    promiseA.then((val) => console.log("asynchronous logging has val:", val));
    console.log("immediate logging");

4.`Destruturing Date`
```jsx
      let a, b, rest;
    [a, b] = [10, 20];
    console.log(a);
    // Expected output: 10
    console.log(b);
    // Expected output: 20
    [a, b, ...rest] = [10, 20, 30, 40, 50];
    console.log(rest);
    // Expected output: Array [30, 40, 50]

```
  

**notes for me**
- The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.A Promise is in one of these states:
       `pending`: initial state, neither fulfilled nor rejected.      
       `fulfilled`: meaning that the operation was completed successfully.      
       `rejected`: meaning that the operation failed.
### Doggos Project [Doggos](file:///C:/Users/PALpro/Downloads/Doggo%20Fetch.html"Doggos")
