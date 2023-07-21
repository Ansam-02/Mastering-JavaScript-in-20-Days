# Day 2: Static Type and Scope
This file summarizes the JavaScript lesson on Static Type and Scope .These Consepts are important in programming, Statically-typed languages perform type checking at compiletime, while dynamically typed languages perform type checking at runtime. The scope is the current context of execution in which values and expressions are "visible" or can be referenced.
Example:

```javascript

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
     const sayHelloWorld: Promise<string> = new Promise((resolve, reject) => {
  resolve("Hello world!");
});

const checkBoolean = (booleanValue: boolean): Promise<boolean> =>
  new Promise((resolve, reject) => {
    if (booleanValue) {
      resolve(booleanValue);
    } else {
      reject(`Input is false :(`);
    }
  });

const returnObj: Promise<{ x: string; y: number }> = new Promise((resolve, reject) => {
  resolve({
    x: "meow",
    y: 45,
  });
});

const promisesArray = [sayHelloWorld, checkBoolean, returnObj];

const convertToObj = async (
  array: Promise<any>[]
): Promise<{ [key: string]: any }> => {
  const obj: { [key: string]: any } = {};

  for (let i = 0; i < array.length; i++) {
    try {
      const result = await array[i];
      obj[`promise${i + 1}`] = result;
    } catch (error) {
      obj[`promise${i + 1}`] = { error: error.message };
    }
  }

  return obj;
};

// Usage
convertToObj(promisesArray).then((result) => {
  console.log(result);
});
```

### SCOPE & HOISTING QUESTIONS:
[Question 1:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
      function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();
```
the answer of the question is (`1, ReferenceError, ReferenceError`), a is declared with `var` which are function scope, meaning they are accessible throughout the whole function, while b and c are declared with let and const which are block-scoped, meaning they are only accessible within the block they are declared in.

[Question 2:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
     

```
[Question 3:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
      

```
