# What I learned from the fourth day tasks
## Example :
> Use Multiple Conditional [Ternary] Operators
   It is considered best practice to format multiple conditional operators such that each condition is on a separate line,
   here is my solution:
   ```javascript
     function checkSign(num) {
      return (num > 0) ? 'positive'
      : (num <0) ? 'negative'
      :'zero';
      }

   ```
> Golf Code
 (Using Multiple Conditional (Ternary) Operators), hers's my solution:
```javascript
  function golfScore(par, strokes) {
  // Only change code below this line
  return strokes==1 
  ? names[0]
  : strokes <= par -2 
  ? names[1]
  : strokes == par -1 
  ? names[2]
  : strokes == par 
  ? names[3]
  :strokes == par +1 
  ? names[4]
  : strokes == par + 2 
  ? names [5]
  : names[6];
 }
```
> Use the map Method to Extract Data from an Array
```jacascript
   
 const ratings = watchList.map(movie =>({
  title : movie['Title'],
  rating :movie["imdbRating"]
 }));

```
> Use the filter Method to Extract Data from an Array
```javascript
      
 const filteredList = watchList.filter(movie => movie.imdbRating >= 8.0).map(movie => ({ title: movie["Title"], rating: movie["imdbRating"] }));
```
   
