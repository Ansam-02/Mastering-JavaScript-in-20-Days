# Day 2: Static Type and Scope

in this day i learned about the difference scopes in js `let`, `const` , `var`
and dive deep into some examples.
also the static type of js which means that JavaScript is a dynamically typed language,
Example:

```javascript
n = true; // n is now a boolean
n = "Hello"; // n is now a string
let n = 99; // n is now a number
```

## Lesson Summary

- Strict mode is generated automatically in js and it make a special behavior.
- Strict mode example:
  ```javascript
  const fun = () => {
    title = "Welcome"; // reference error
    console.log(title);
  };
  ```
- The code above reference an error deo to strict mode.
- Undefined: means that it's declared but it's dose not have any value.
- Declared: means that it's has never declared on the whole program.

## Coding Example

```javascript
  var teacher = "khaldoon"

  function otherClass(){
      vat teacher = "shadi"
      console.log("Welcome")
  }

  function ask(){
      var = question = "why?";
      console.log(question)
  }

  otherClass()
  ask()

```
## Coding Exercies
### STATIC TYPING QUESTIONS:

[Question 1:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
     

```

### SCOPE & HOISTING QUESTIONS:
[Question 1:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
      

```
[Question 2:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
     

```
[Question 3:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
      

```
