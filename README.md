# Number Guessing Game in C

## Overview
This program implements a simple number guessing game in C. The goal of the game is for the player to guess a randomly generated number between 1 and 100. The player has a maximum of 10 attempts to guess the number. After each guess, the program provides feedback on whether the guess is too high or too low. If the player guesses the correct number or exhausts their attempts, the game ends.

## Features
- Random number generation between 1 and 100.
- The player is allowed up to 10 attempts to guess the number.
- After each guess, feedback is provided to indicate if the guess is too high or too low.
- If the player guesses correctly, the number of attempts is displayed.
- If the player runs out of attempts, the program reveals the correct number.

## Code Breakdown

1. **Libraries**:
   - `stdio.h`: Used for input and output operations.
   - `stdlib.h`: Provides functions for random number generation.
   - `time.h`: Used to seed the random number generator.

2. **Variables**:
   - `numberToGuess`: Holds the randomly generated number that the player has to guess.
   - `userGuess`: The player's current guess.
   - `attempts`: Tracks the number of attempts the player has made.
   - `maxAttempts`: Constant that defines the maximum number of allowed attempts (set to 10).

3. **Random Number Generation**:
   - The `srand(time(0))` function seeds the random number generator using the current time.
   - `numberToGuess = (rand() % 100) + 1;` generates a random number between 1 and 100.

4. **Gameplay Loop**:
   - The program repeatedly asks the player to input a guess.
   - If the guess is correct, the program congratulates the player and ends.
   - If the guess is too low or too high, the program prompts the player to try again.
   - If the player runs out of attempts, the game reveals the correct number and ends.

## Example Output
Welcome to the Number Guessing Game!
Enter your guess (1-100): 50 
Too low. Try again. 
Enter your guess (1-100): 75 
Too high. Try again. 
Enter your guess (1-100): 60
Congratulations! You guessed the number in 3 attempts.
