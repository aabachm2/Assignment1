# Number Guessing Game

## Initial Repo Structure

It looks like there are 5 branches at the start of this project (6 if you include documentation):

- dev: branches off main. Currently just adds a "good luck" message.
- feature1: branches off main. Adds functionality to quit using a negative number, a "do you want to play again" dialog, and tests.
- feature2: branches off dev. It includes the encouraging message, and goes on to changes the game to have a maximum number of attempts (hard-coded at 10), and a "game over" state if the player runs out of guesses.
- feature3: branches off main. Adds a hint indicating not just if the player was too high or too low, but also how far away they were from the target number, and tests.
- hotfix: branches off main. Fixes an off-by-one error in the randomInt() method, so it includes the maximum value, and adds tests.
- documentation: this branch, mostly concerned with the README.

## Lessons Learned

After all that, I think the best way to resolve merge conflicts is to NOT HAVE MERGE CONFLICTS.

Merging is (for me) the baseline way to combine two branches. It will keep pointers to multiple parent branches, so a branch will start to develop a non-linear history. Rebasing is a good way to keep it linear. If thingA and thingB both happened at the same time, merging preserves both parents, but rebasing is explicitly deciding thingA happened, and THEN thingB happened. Squashing is a good way to have frequent intermediate commits AND have a clean log at the same time. Cherry-picking is a good way to apply a single fix.

Looking at the git logs, feature1 got removed, feature2 and feature3 are mostly-linear, though there is still branching going on that makes it a little confusing to look at.

In a real project:

- Messy partial commits should be squashed as you go along. When a step has been completed on a branch, the intermediate commits should be squashed into a summary.
- Rebasing is a good way to keep a history linear. It should be used anytime you're cleaning up a branch, e.g. hiding the mess of a feature branch before merging it into dev. This should be the go-to operation, I think.
- Cherry-picking should only be used for hotfixes.
- Merging should really only be used when you can fast-forward, otherwise you get a nonlinear history that will bleed into whatever you're merging into.
