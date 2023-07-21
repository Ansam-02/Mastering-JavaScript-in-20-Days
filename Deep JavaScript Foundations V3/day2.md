# Day 2: Static Type and Scope
This file summarizes the JavaScript lesson on Static Type and Scope .These Consepts are important in programming, Statically-typed languages perform type checking at compiletime, while dynamically typed languages perform type checking at runtime. The scope is the current context of execution in which values and expressions are "visible" or can be referenced.

## Lesson Summary

- In statically typed languages, variable types are explicitly defined and checked at compile-time rather than runtime.
- Variables must be declared with a specific type, and their type cannot be changed during execution.
- Static typing provides early detection of type-related errors, which can lead to more robust and secure code.
- Scope refers to the visibility and accessibility of variables within a program.
- Common scope types include global scope, function scope, and block scope (introduced with let and const).
- Global scope: Variables declared outside of any function or block can be accessed from any part of the code.
- Function scope: Variables declared inside a function can only be accessed within that function.
- Block scope: Variables declared with let and const inside a block (e.g., within loops or if statements) can only be accessed within that block.


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
the answer of the question is (`1, ReferenceError, ReferenceError`), a is declared with `var` which are function scope, meaning they are accessible throughout the whole function, while b and c are declared with `let` and `const` which are block-scoped, meaning they are only accessible within the block they are declared in.

[Question 2:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
     function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();
```
the answer of the question is (`undefined, ReferenceError, ReferenceError`), a is declared with `var` which are function scope, meaning they are accessible throughout the whole function, while b and c are declared with `let` and `const` which are block-scoped, meaning they are only accessible within the block they are declared in.
[Question 3:](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)
```jsx
      
 function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
  }

 testScope3();
```
the answer of the question is  m   ` [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1,100, 45 ]`, variables are declared with `var` which are function scope, meaning they are accessible throughout the whole function, while variables are declared with `let` and `const` which are block-scoped, meaning they are only accessible within the block they are declared in.


