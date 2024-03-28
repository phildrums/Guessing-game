function checkGuess() {
  var secretNumber = Math.floor(Math.random() * 100) + 1;
  var guess = parseInt(document.getElementById("guessInput").value);
  var result = document.getElementById("result");

  if (isNaN(guess)) {
    result.innerHTML = "Please enter a valid number.";
    return;
  }

  if (guess === secretNumber) {
    result.innerHTML = "Congratulations! You've guessed the number.";
  } else if (guess < secretNumber) {
    result.innerHTML = "Too low! Try again.";
  } else {
    result.innerHTML = "Too high! Try again.";
  }
}
