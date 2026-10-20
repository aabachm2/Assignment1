# Number Guessing Game

## Initial Repo Structure

It looks like there are 5 branches at the start of this project (6 if you include documentation):

- dev: branches off main. Currently just adds a "good luck" message.
- feature1: branches off main. Adds functionality to quit using a negative number, a "do you want to play again" dialog, and tests.
- feature2: branches off dev. It includes the encouraging message, and goes on to changes the game to have a maximum number of attempts (hard-coded at 10), and a "game over" state if the player runs out of guesses.
- feature3: branches off main. Adds a hint indicating not just if the player was too high or too low, but also how far away they were from the target number, and tests.
- hotfix: branches off main. Fixes an off-by-one error in the randomInt() method, so it includes the maximum value, and adds tests.
- documentation: this branch, mostly concerned with the README.
