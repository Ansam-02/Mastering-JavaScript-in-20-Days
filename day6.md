 **Part One**
 ## The DOM
Document Object Model: The HTML DOM document object is the owner of all other objects in your web page.
we work with different methods as getElementById, getElementsByTagName, getElementsByClassName, and querySelector..
```javascript
  document.querySelector("#p1-name").textContect
```
```javascript
  document.getElementById("p2-symbol").textContect = 'X'
```
```javascript
 document.querySelector("header h2").textContect=" A game You Know and like"
```



## Strings
A JavaScript string is zero or more characters written inside quotes.
```javascript
  document.querySelector("#p1-name").append(" Ansam ")
```
```javascript
  document.title
  document.title.indexOf("T")
```
```javascript
 document.querySelector("header h1").textContect.toUpperCase()
```
## Arrays
An array is a special variable, which can hold more than one value

## Objects
Objects can also have methods.
Methods are actions that can be performed on objects.
Methods are stored in properties as function definitions.
```javascript
  const ansam ={
    name:"Ansam",
    home:"Palestine",
    pet: "cat",
    hobbies: ['photography','Painting','OutDoor Activites','Volunteer Work']
   };
```
#### Quiz Project
```javascript
    const statement = document.getElementById('statment');
    // optionButtons should be all the elements within the "options" div
    const optionButtons = document.querySelector("#options");
    // explanation should be the "explanation" div
    const explanation = document.getElementById("explanation");
// TODO 2: Declare & assign a variable called fact
    // Its value should be an object with a statement, true/false answer, and explanation 
    const fact ={
        statement:"Arrays are like object",
        answer: true,
        explanation: "Array are a kind of object with special proparties"
    };    
    // TODO 3: Set the text of the statement element to the fact's statement
    statement.textContent =fact.statement;

    // TODO 4: Declare disable & enable functions to set or remove the "disabled" attribute from a given button element
    // disable(button) should set the button element's attribute "disabled" to the value ""
    // enable(button) should remove the attribute "disabled" from the button element
    const disable = (button)=>{
        button.setAttribute('disable',"");
    }
    const enable = (button)=> button.removeAttribute("disabled");
    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
    const isCorrect=(guess)=>{return guess=== fact.answer};
    
```
## Events
events are "things" that happen to HTML elements, When JavaScript is used in HTML pages, JavaScript can "react" on these events.


