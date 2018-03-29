# Matrices

Matricies are also reffered to as Two Dimensional Arrays which are essentially rows and columns.

They are frequently used data structures for a wide variety of applications including:

- Representing a grid (Chess Boards, tic-tac-toe, etc).
- 3D Rendering.
- Physics.
- Statistics.
- Machine Learning.

## Building Battleship

A 5x5 board can be created as follows:

``` js
var board {
  [null, null, null, "S", null],
  [null, "S", null, "S", null],
  ["S", null, null, null, null],
  [null, "S", null, null, null],
  [null, null, null, null, "S"]
}
```

``` js
var board = [
  [null, null, null, "S", null],
  [null, "S", null, "S", null],
  ["S", null, null, null, null],
  [null, "S", null, null, null],
  [null, null, null, null, "S"]
]
```
Consider that the inner loop(j) will run for as many columns there are in a row. 
The outer loop(i) will run for as many rows there are in the matrix.

``` js
for (var i = 0; i < board.length; i++)
{
  // A single row, such as board[0], board[1], board[2]
  var row = board[i];
  // Loop over each element in the row
  // We use "j" because "i" is already being used.
  // What would happen if we used i in this loop instead? Try it.
  for (var j = 0; j < row.length; j++){
    var column = row[j];
    // If the column is a ship, log the coords
    if (column === "S"){
      console.log("Ship found at: " + i + ", " + j);
    }
    // Instead of using variables, you could reference: board[i][j]
  }
}
``` 

``` js
var board = [ // Lays out our 5x5 grid.
  [null, null, null, "S", null],
  [null, "S", null, "S", null],
  ["S", null, null, null, null],
  [null, "S", null, null, null],
  [null, null, null, null, "S"]
]

// Iterates 10 turns. 
for (var i = 0; i < 10; i++)
{
  var row = getRandomNum();
  var column = getRandomNum();
  console.log("Row " + row + " " + "Column " + column);
  var randomSquare = board[row][column];
  
  if(randomSquare === "S"){
    console.log("Ship sunk on " + row + ", " + column);
    board[row][column] = null; // Sets a sunken ship to null.
  }
}

function getRandomNum(){
  return Math.floor(Math.random() * 5); // Allows us to get a random number 0-4 instead of 0-1
}
```