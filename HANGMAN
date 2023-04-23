const input = require('sync-input')


console.log(`H A N G M A N`);
console.log();
let arrOfAnswers = ["python", "java", "swift", "javascript"];
let theChosenOne = arrOfAnswers[Math.floor(Math.random() * arrOfAnswers.length)];
let helper2 = theChosenOne.replace(/./g,"-");
let workingArr = helper2.split("");
let previousGuesses = [];
let attempts = 0;
while (true) {
  if (attempts < 8 && workingArr.join("").toString() != theChosenOne) {
    console.log(workingArr.join("").toString());
  }

  if (workingArr.join("").toString() == theChosenOne) {
    console.log(`You guessed the word ${theChosenOne}!\nYou survived!`)
    break;
  }
    if (attempts == 8) {
    console.log("\nYou lost!");
      break;
  }
let letter = input("Input a letter:");

  if (letter.split("").length > 1 || letter === "") {
    console.log("Please, input a single letter.");
    continue;
  }
  if (letter !== letter.toLowerCase() || letter.match(/[^a-z]/gi)) {
    console.log("Please, enter a lowercase letter from the English alphabet.");
    continue;
  }
  
    if (previousGuesses.includes(letter)) {
    console.log("You've already guessed this letter.");
    attempts = attempts + 1;
    continue;
  }
  
  if (theChosenOne.includes(letter)) {
    let firstOccurence = theChosenOne.indexOf(letter);
    let lastOccurence = theChosenOne.lastIndexOf(letter);
    workingArr[firstOccurence] = letter;
    workingArr[lastOccurence] = letter;
    previousGuesses.push(letter);
    continue;
} 

else {
    previousGuesses.push(letter)
    console.log("That letter doesn't appear in the word.\n")
  attempts = attempts + 1;
    continue;
  }
}
