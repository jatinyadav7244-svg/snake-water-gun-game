import random

def snake_water_gun():
    print("Welcome to Snake–Water–Gun Game!")
    print("Rules: Snake vs Water -> Snake wins | Water vs Gun -> Water wins | Gun vs Snake -> Gun wins\n")

    choices = ['snake', 'water', 'gun']
    user_choice = input("Enter your choice (snake/water/gun): ").lower()

    if user_choice not in choices:
        print("Invalid choice! Please select from snake, water, or gun.")
        return

    comp_choice = random.choice(choices)
    print(f"Computer chose: {comp_choice}")

    if user_choice == comp_choice:
        print("It's a draw!")

    elif (user_choice == 'snake' and comp_choice == 'water') or \
         (user_choice == 'water' and comp_choice == 'gun') or \
         (user_choice == 'gun' and comp_choice == 'snake'):
        print("🎉 You win!")

    else:
        print("😢 You lose!")

# Run the game
snake_water_gun()
    
