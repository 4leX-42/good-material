# Guess the number game by ArbustorojoGH

import random

# Define game settings
MAX_NUMBER = 100
MAX_GUESSES = 7

# Generate random number
number = random.randint(1, MAX_NUMBER)

# Print game instructions
print("Guess the number between 1 and", MAX_NUMBER)
print("You have", MAX_GUESSES, "guesses")

# Loop until player guesses correctly or runs out of guesses
for guess_count in range(1, MAX_GUESSES + 1):
    # Read input from user
    guess = input("Guess #" + str(guess_count) + ": ")
    guess = int(guess)

    # Check if guess is correct
    if guess == number:
        print("Congratulations, you guessed the number!")
        break

    # Provide feedback on guess
    if guess < number:
        print("Too low, try again")
    else:
        print("Too high, try again")

    # Check if player is out of guesses
    if guess_count == MAX_GUESSES:
        print("Sorry, you ran out of guesses")
        print("The number was", number)
