# What I learned from the first day tasks
I done a simple tasks which about the basic of javascribt and Basic Data Structure
## Example:
#### Expressions
1) Profile Lookup
   A lookUpProfile function that takes firstName and a property (prop) as arguments has been pre-written for you.
   ```javascript
    const contacts = [
    {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
    },
   {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
  ];

  function lookUpProfile(name, prop) {
  // Only change code below this line
  
 for (let i = 0; i < contacts.length; i++) {
    if (contacts[i].firstName === name) {
      if (prop in contacts[i]) {
        return contacts[i][prop];
      } else {
        return "No such property";
      }
    }
  }

   return "No such contact";
      // Only change code above this line
     }

   lookUpProfile("Akira", "likes");
```
#### Arrays
2) Copy Array Items Using slice()
   let fruits = ['apple', 'banana', 'grips', 'melon', 'peach'];
    let myfavfruits = fruits.slice(1, 3);
#### Objrcts
3) Combine Arrays with the Spread Operator
   function spread() {
  let fullname= ['Ansam', 'Jadayel'];
  let sentence = ['My','Full','Name','is',...fullname];
  return sentence;
}

console.log(spread());
