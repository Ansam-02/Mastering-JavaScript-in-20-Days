
# Day 5: Rick & Morty
> Create a web page that fetches data from the Rick and Morty API, and displays a list of characters.

# What i learn
- I learned how to fetch data from API.
- how to filter it by category, and also how to search for a specific item by its name.

## html Code
 ```html
  <!DOCTYPE html>
  <html>
  <head>
  <title>Alive Character List</title>
  <link rel="stylesheet" href="./styles.css">

  </head>
  <body>
  <h1>Alive Character List</h1>
  <ul id="characterList"></ul>

  <script src="./script.js"></script>
  </body>
  </html>

```
## css Code
```css

  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
  }
  
  h1 {
    text-align: center;
  }
  
  ul#characterList {
    list-style-type: none;
    padding: 0;
  }
  
  ul#characterList li {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  
  ul#characterList li img {
    width: 100px;
    height: 100px;
    object-fit: cover;
    margin-right: 10px;
  }
  
  ul#characterList li h2 {
    margin: 0;
    font-size: 18px;
  }
  
  ul#characterList li p {
    margin: 5px 0;
    font-size: 14px;
  }
  

```
## javascript Code
```jsx

  const characterList = document.getElementById('characterList');

   async function fetchCharacters() {
      try {
        const response = await fetch('https://rickandmortyapi.com/api/character?status=alive');
        if (!response.ok) {
            throw new Error('Error ');
        }
        const body = await response.json();
        const characters = body.results.slice(0, 50);

        characters.forEach(character => {
            const li = document.createElement('li');
            li.innerHTML = `
        <img src="${character.image}" alt="${character.name}">
        <div>
          <h2>${character.name}</h2>
          <p>Location: ${character.location.name}</p>
          <p>Species: ${character.species}</p>
          <p>Gender: ${character.gender}</p>
        </div>
      `;
            characterList.appendChild(li);
        });
    } catch (error) {
        console.error(error);
        characterList.innerHTML = 'Error ';
    }
  }

  fetchCharacters();

```
![]()

> ![image](https://github.com/Ansam-02/Mastering-JavaScript-in-20-Days/assets/137777479/86608f6a-aae0-4772-8e67-9bd70c928fb3)
