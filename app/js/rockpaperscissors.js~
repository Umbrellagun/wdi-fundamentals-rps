////////////////////////////////////////////////
/*   Provided Code - Please Don't Edit   */
////////////////////////////////////////////////
'use strict';

function getInput() {
    console.log("Please choose either 'rock', 'paper', or 'scissors'.");
    return prompt();
}
function randomPlay() {
    var randomNumber = Math.random();
    if (randomNumber < 0.33) {
        return "rock";
    } else if (randomNumber < 0.66) {
        return "paper";
    } else {
        return "scissors";
    }
}
////////////////////////////////////////////////
/*           Write Your Code Below            */
////////////////////////////////////////////////

//ensures user move
function getPlayerMove(move) {
    return (move || getInput());
}

//ensures computer move
function getComputerMove(move) {
    return (move || randomPlay());
}

function getWinner(playerMove, computerMove) {
    var winner;

    if(playerMove == computerMove) {
        winner = "tie";
    } else if (computerMove == "rock" && playerMove == "scissors") {
        winner = "computer";
    } else if (computerMove == "scissors" && playerMove == "paper") {
        winner = "computer";
    } else if (computerMove == "paper" && playerMove == "rock") {
        winner = "computer";
    } else {
        winner = "player";
    }
  
    return winner;
}

function playToFive() {
    console.log("Let's play Rock, Paper, Scissors");
    var playerWins = 0;
    var computerWins = 0;

    while (playerWins < 5 && computerWins < 5) {

        var winner = getWinner(getPlayerMove(), getComputerMove());
        var message = "";        

        if(winner == "player"){
            message = "You won!";
            playerWins++;
        } else if(winner == "computer"){
            message = "You lost. :(";
            computerWins++;
        } else {
            message = "It's a tie, try again!";
        }
  
     console.log("Player chose " + getPlayerMove() + " and Computer chose " + getComputerMove());
     console.log(message);
     console.log("Player wins: " + playerWins);
     console.log("Computer wins: " + computerWins);
    }

   return [playerWins, computerWins];

}

playToFive();

