# Day 4: Classes & Prototypes (oop)
This file has described the basic features of class-based object oriented programming, and briefly looked at how JavaScript constructors and prototypes compare with these concepts.

## Lesson Summary
- Understanding Classes.
- Describe the components of a class, such as attributes (data) and methods (functions).
- Understanding the difference between `__proto__` and `prototype`.
- How to use a technique called inheritance. 
- DRY principle.
## Coding Example

```javascript
  class UserCreator {
   constructor (name, score){
   this.name = name;
   this.score = score;
   }
   increment (){ this.score++; }
   login (){ console.log("login"); }
  }
  const user1 = new UserCreator("Eva", 9);
  user1.increment();

```

#### My Solution

 ### [FreeCodeCamp](https://www.freecodecamp.org/fcc2f876d96-f90f-4083-9243-b9a152b65974)
