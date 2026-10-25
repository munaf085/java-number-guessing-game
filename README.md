# Build a number guessing game

A number guessing game. The computer picks a secret number from 1 to 100. The player has 7 attempts, and after each guess the program says `Too high!` or `Too low!`.

## Features

- Pick a random secret number from 1 to 100 for every round.
- When started with a number, like `java GuessingGame 42`, use it as the seed of `Random` so the game can be replayed exactly (MentorNxt's hidden tests do this); started without one, pick truly random numbers.
- Read guesses with `Scanner` and print `Too high!`, `Too low!` or `Correct!`.
- Allow at most 7 attempts, then show the secret number.
- Do not count guesses outside 1 to 100; ask again instead.
- Show how many attempts the player used.
- Ask `Play again? (y/n)` and start a new round on `y` or `Y`.

## How to run

```
javac GuessingGame.java
java GuessingGame
```

## Sample run

```
=== Number Guessing Game ===

I am thinking of a number from 1 to 100.
You have 7 attempts.
Your guess: 50
Too high!
Your guess: 25
Too low!
Your guess: 150
Please guess a number from 1 to 100.
Your guess: 37
Too high!
Your guess: 35
Correct! Attempts used: 4
Play again? (y/n): n
Thanks for playing!
```

## What I used

- A random number maker: `new Random()` and `nextInt(100) + 1`
- A [`while` loop](/learn/java/basics/loops/while-and-do-while) with two conditions joined by `&&`
- [`continue`](/learn/java/basics/loops/break-and-continue) to skip a bad guess
- A `do-while` loop for "play again"
- [Methods with parameters](/learn/java/basics/methods/parameters-and-arguments) and a `boolean` return value
- [`equalsIgnoreCase`](/learn/java/basics/strings/string-equals-vs-double-equals) to accept `y` or `Y`
- Counting with [`attempts++`](/learn/java/basics/operators/increment-and-decrement)
- The `args` of `main`: a number typed after the class name when the program starts

## Author

Your name
