# Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> |Generate random number| GenerateNumber[/Random Number/]
    GenerateNumber --> |Prompt user for input| GetInput[/User Input/]
    GetInput --> |Is input valid?| ValidateInput{Valid Input?}
    ValidateInput --> |Yes| CompareInput{Guess Correct?}
    ValidateInput --> |No| InvalidInput[/Invalid Input. Try Again/]
    InvalidInput --> GetInput
    CompareInput --> |Yes| SuccessMessage[/Correct! You Won!/] --> End([End])
    CompareInput --> |No| HighLow{Too High or Too Low?}
    HighLow --> |Too High| TooHighMessage[/Too High, Try Again/]
    HighLow --> |Too Low| TooLowMessage[/Too Low, Try Again/]
    TooHighMessage --> GetInput
    TooLowMessage --> GetInput

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
