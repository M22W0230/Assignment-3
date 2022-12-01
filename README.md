# Assignment-3

<!DOCTYPE html>
<html lang="en">
<meta charset="UTF-8">
<title>Page Title</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<link rel="stylesheet" href="">
<style>
</style>
<script type="text/javascript">
"use strict"
//PART 1
//1,2 & 3 create class , constructor and property, life should be 3 when create an instance
class Player {
  constructor(name) {
    this.name = name;
    this.lives = 3;
  }
  //4a loose life method
  looseLife() {
    console.log(this.lives);
    if (this.lives <= 1) {
      console.log("Game Over")
      return 0;
    } else {
      console.log("You have lost one life");
      return this.lives -= 1;
    }
  }

  //4b Remaining lives method
  numberOfLives() {
    return "You have  total of " + this.lives + " lives left"
  }
}
//New instance
const player1 = new Player("Sudip");
console.log("Welcome " + player1.name + " You have  total of " + player1.lives + " lives");

//Loose First Life
player1.lives = player1.looseLife();
console.log(player1.numberOfLives());

//Loose Second Life 
player1.lives = player1.looseLife();
console.log(player1.numberOfLives());

//loose third Life - GAME OVER !!!
player1.lives = player1.looseLife();
console.log(player1.numberOfLives());

//loose life again - No Negative number test
player1.lives = player1.looseLife();
console.log(player1.numberOfLives());

//PART 2
const numbers1 = {
  numberOne: 12,
  numberTwo: 15
};

const numbers2 = {
  numberOne: -5,
  numberTwo: 4
};

function getObjectWithMaxSumOfNumbers(numbers1, numbers2) {
  let sum1 = sum(numbers1);
  let sum2 = sum(numbers2);
  if (sum1 > sum2) {
    return numbers1;
  } else {
    return numbers2;
  }
}

function sum(obj) {
  var sum = 0;
  for (var el in obj) { //iterate throgh elements in Objects
    if (obj.hasOwnProperty(el)) {
      sum += parseFloat(obj[el]); // get the element from object and add to sum
    }
  }
  return sum;
}

let objectWithMaxSum = getObjectWithMaxSumOfNumbers(numbers1, numbers2);
console.log(objectWithMaxSum);

</script>
<body>


<div class="">
Assignment By Sudip Khadka

</div>

</body>
</html>
