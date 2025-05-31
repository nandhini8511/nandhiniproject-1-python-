# nandhiniproject-1-python-
import random

def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

def determine_winner(player, computer):
    if player == computer:
        return "It's a tie!"
    elif (player == 'rock' and computer == 'scissors') or \
         (player == 'scissors' and computer == 'paper') or \
         (player == 'paper' and computer == 'rock'):
        return "You win!"
    else:
        return "Computer wins!"

def play_game():
    print("Welcome to Rock-Paper-Scissors!")
    options = ['rock', 'paper', 'scissors']
    while True:
        player_choice = input("Enter your choice (rock, paper, scissors) or 'q' to quit: ").lower()
        if player_choice == 'q':
            break
        if player_choice not in options:
            print("Invalid choice. Please choose rock, paper, or scissors.")
            continue
        computer_choice = get_computer_choice()
        print(f"\nYou chose: {player_choice}")
        print(f"Computer chose: {computer_choice}")
        result = determine_winner(player_choice, computer_choice)
        print(result)
        print()  # Empty line for better readability

play_game()