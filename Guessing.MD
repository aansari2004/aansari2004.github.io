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
### Guessing Game Flowchart Explanation

1. **Start**: The program begins and initializes the game.
2. **GenerateNumber**: The program generates a random number within a specified range (e.g., 1 to 100).
3. **GetInput**: The user is prompted to enter a guess.
4. **ValidateInput**: The program checks if the user's input is valid (numeric and within the correct range).
    - If the input is invalid, the program prompts the user to enter a valid guess.
5. **CompareInput**: The program compares the user's guess to the random number.
    - If the guess is correct, the game ends, and the program displays a success message.
    - If the guess is too high or too low, the program informs the user and prompts for another guess.
6. **Repeat**: The process repeats until the user guesses the correct number.
7. **End**: The game ends when the user guesses the correct number.
