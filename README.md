# guess_the_number.py
guess_the_number.py
import random

# Generate a random number between 1 and 100
secret_number = random.randint(1, 100)

# Initialize variables
attempts = 0
max_attempts = 10

print("Welcome to the Guess the Number game!")
print("I'm thinking of a number between 1 and 100.")

while attempts < max_attempts:
    try:
        guess = int(input("Take a guess: "))

        if guess < secret_number:
            print("Higher!")
        elif guess > secret_number:
            print("Lower!")
        else:
            print(f"Congratulations! You guessed the number {secret_number} in {attempts + 1} attempts.")
            break

        attempts += 1

    except ValueError:
        print("Please enter a valid number.")

if attempts >= max_attempts:
    print(f"Sorry, you've reached the maximum number of attempts. The secret number was {secret_number}. Try again!")

