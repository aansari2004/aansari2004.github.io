# Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start Game]) --> GenerateRandomNumber[Generate Random Number]
    GenerateRandomNumber --> GetUserGuess[Get User Guess]
    GetUserGuess --> CheckIfValidInput{Is Input Valid?}
    CheckIfValidInput -- No --> ErrorMessage[Display "Invalid Input, Try Again"]
    ErrorMessage --> GetUserGuess
    CheckIfValidInput -- Yes --> CheckIfCorrectGuess{Is Guess Correct?}
    CheckIfCorrectGuess -- No, Too High --> TooHigh[Display "Too High"]
    TooHigh --> GetUserGuess
    CheckIfCorrectGuess -- No, Too Low --> TooLow[Display "Too Low"]
    TooLow --> GetUserGuess
    CheckIfCorrectGuess -- Yes --> Congratulations[Display "Congratulations!"]
    Congratulations --> PlayAgain{Play Again?}
    PlayAgain -- Yes --> GenerateRandomNumber
    PlayAgain -- No --> EndGame([End Game])
