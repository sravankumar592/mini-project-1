# mini-project-1
python

   import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("You will select a range [X, Y] and try to guess the number.")
    print("Let's get started!")
    
    # Input range from the user
    X = int(input("Enter the lower bound X: "))
    Y = int(input("Enter the upper bound Y: "))
    
    # Validate that X < Y
    if X >= Y:
        print("Invalid range. Please ensure X < Y.")
        return
    
    # Generate a random number in the range [X, Y]
    target = random.randint(X, Y)
    
    # Initialize variables
    guesses = 0
    guessed_correctly = False
    
    # Game loop
    while not guessed_correctly:
        guess = int(input("Make a guess: "))
        guesses += 1
        
        if guess < target:
            print("Too low! Try again.")
        elif guess > target:
            print("Too high! Try again.")
        else:
            print(f"Congratulations! You guessed the number {target} correctly in {guesses} guesses.")
            guessed_correctly = True

# Start the game
number_guessing_game()

output:

      Welcome to the Number Guessing Game!
You will select a range [X, Y] and try to guess the number.
Let's get started!
Enter the lower bound X: 6
Enter the upper bound Y: 8
Make a guess: 8
Too high! Try again.
Make a guess: 6
Too low! Try again.
Make a guess: 7
Congratulations! You guessed the number 7 correctly in 3 guesses.

=== Code Execution Successful ===
