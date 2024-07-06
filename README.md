const getUserChoice = (userInput) => {
  userInput = userInput.toLowerCase();
  if (
    userInput === "rock" ||
    userInput === "paper" ||
    userInput === "scissors"
  ) {
    return userInput;
  } else {
    console.log(
      "No correct input!,you need to write (rock,papper or scissors)"
    );
  }
};
//USER CHOICE!

const getComputerChoice = () => {
  let choice = Math.floor(Math.random() * 3);
  switch (choice) {
    case 0:
      choice = "rock";
      break;
    case 1:
      choice = "paper";
      break;
    case 2:
      choice = "scissors";
      break;
  }
  return choice;
};
//COMPUTER CHOICE!

function determineWinner(userChoice, computerChoice) {
  if (userChoice === computerChoice) {
    return "Draw";
  } else if (userChoice === "paper" && computerChoice === "scissors") {
    return "Computer WIN!";
  } else if (userChoice === "rock" && computerChoice === "paper") {
    return "Computer WIN!";
  } else if (userChoice === "scissors" && computerChoice === "rock") {
    return "Computer WIN!";
  } else if (userChoice === "rock" && computerChoice === "paper") {
    return "Computer WIN!";
  } else {
    return "User WIN!";
  }
}
const playGame = () => {
  let userChoice = getUserChoice('rock');
  let computerChoice = getComputerChoice();
  getUserChoice(userChoice);
  getComputerChoice(computerChoice);

  console.log(getUserChoice(userChoice));
  console.log(getComputerChoice(computerChoice));
  console.log(determineWinner(userChoice, computerChoice));
};
playGame();