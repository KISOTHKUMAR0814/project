import random
def rockpaperscissors():
    print("Welcome to Rock, Paper, Scissors!")
    print("Instructions: Type 'rock', 'paper', or 'scissors' to play. Type 'exit' to quit the game.")

    choices = ["rock", "paper", "scissors"]
    while True:
        playerchoice = input("Your choice: ").lower()
        if playerchoice == "exit":
            print("Thanks for playing! Goodbye!")
            break
        if playerchoice not in choices:
            print("Invalid choice. Please choose 'rock', 'paper', or 'scissors'.")
            continue
        computerchoice = random.choice(choices)
        print("Computer chose:",computerchoice)
        if playerchoice == computerchoice:
            print("It's a tie!")
        elif (playerchoice == "rock" and computerchoice == "scissors") or \
             (playerchoice == "scissors" and computerchoice == "paper") or \
             (playerchoice == "paper" and computerchoice == "rock"):
            print("You win!")
        else:
            print("You lose!")
rockpaperscissors()
