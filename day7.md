
## Map & Filter 
methods let us process all the items in an array
map: applies some kind of operations on all the array's elements.
filter: filter out the ingredients i dont want from the array.
1. create a new array with only the names of the girls
```jsx
      const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
            ];

    const names = spices.map(s=> spices.name);
```
2. create a new array endINY with the girls whose nicknames end with 'y'
```jsx
    const endINY = spices.filter(s=>s.nickname[s.nicknames.length-1 ]=== 'y');
```
