
# Day 7: JavaScript: Modules, Debugging, Error Handling and More
 Its include `Modules` which allow you to break up your code into separate files. This makes it easier to maintain a code-base. and `Debugging`  is the process of finding and fixing errors or bugs in the source code of any software.`Error-handling` mechanism to catch runtime errors using try-catch-finally block,



## Lesson Summary 📝📝

- Modules are imported from external files with the import statement.
-modules also rely on type="module" in the <script> tag.
- way to understand what's heppening when your program runs:
 (console.log(),console.warn(), console.error()and using the browser's built debbugger.
- Browser's debuggers work as firefox,chrome.
- The try statement allows you to define a block of code to be tested for errors while it is being executed.
- The catch statement allows you to define a block of code to be executed, if an error occurs in the try block.
- JavaScript Frameworks provide pre-written code and tools, making the development process faster and easier than Vanilla JavaScript.
-  React provides a virtual DOM that allows for faster updates and easier manipulation of the UI.
-  

## Coding Example ✨
```jsx
    //example on error handling
    try {
    thisMightThrowAnError();
  } catch (error) {
      console.error("As if! Error:", error); 
      console.log("Whatever, let's press on anyway");
      }
      console.log("still rollin' with the homies");
```

