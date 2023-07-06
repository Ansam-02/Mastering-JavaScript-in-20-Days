 **Part One**
day5 I start the first course JavaScript from First Steps to Proffessional
 ## The DOM
Document Object Model: The HTML DOM document object is the owner of all other objects in your web page.
we work with different methods as getElementById, getElementsByTagName, getElementsByClassName, and querySelector..
here's the the exercies that i solved:
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
here's the the exercies that i solved:
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
here's the the exercies that i solved:
```javascript
  const ansam ={
    name:"Ansam",
    home:"Palestine",
    pet: "cat",
    hobbies: ['photography','Painting','OutDoor Activites','Volunteer Work']
   };
```
#### Quiz Project
here's the the exercies that i solved of the Quiz project:
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

    // TODO 4: Declare disable & enable functions to set or remove the "disabled" attribute from a given   button element
    // disable(button) should set the button element's attribute "disabled" to the value ""
    // enable(button) should remove the attribute "disabled" from the button element
    const disable = (button)=>{
        button.setAttribute('disable',"");
    }
    const enable = (button)=> button.removeAttribute("disabled");
    // TODO 5: Declare an isCorrect function that compares a guess to the right answer
    // isCorrect(guess) should return true if the guess matches the fact's answer
    const isCorrect=(guess)=>{return guess=== fact.answer};
      // TODO 6A: Use a for loop to add a click event listener to each of the optionButtons
    for(let button of optionButton){
        button.addEventListener("click",(event) =>{

       
            // TODO 6B: Within the event handler function, display the fact's explanation by setting the     text of the explanation element
            explanation.textContent = fact.explanation;
            // TODO 7: Within the event handler function, 
            // Use a for loop to disable all the option buttons
          
            for(let otherbutton of optionButtons){
                disable(otherbutton);
            }

            // TODO 8: Within the event handler function,
            // Get the guessed value from the clicked button
            // Use a conditional to compare the guess to the fact's answer
            // and add the "correct"/"incorrect" class as appropriate
            if(isCorrect(button.value)){
                button.classList.add("correct");
            }else {
                button.classList.add("incorrect");
            }
        })
    }

    
```
## Events
events are "things" that happen to HTML elements, When JavaScript is used in HTML pages, JavaScript can "react" on these events.here's the the exercies that i solved:
1. capitilize the text of the button 'true'.
```jsx
 let trueButton;
 trueButton.addEventListener('click',(event)=>{
 trueButton.textContext = trueButton.textContext.toUpperCase();
 });
```
2. change h1 to 'hovering' when the mouse moves into the element
```jsx
 h1.addEvenrListener('mouseover',(event)=>{
    h1.textContect="hovering";
 });
```
3. change h1 to 'Quiz.js' when the mouse moves out the element
```jsx
 h1.addEvenrListener('mouseout',(event)=>{
    h1.textContect="Quiz.js";
 });
```
## Loop
Loops can execute a block of code a number of times.
* disable loop project exercies
```jsx
    for(let button of optionButton){
        button.addEventListener("click",(event) =>{
            explanation.textContent = fact.explanation;

            for(let otherbutton of optionButtons){
                disable(otherbutton);
            }
        })
    }

```
