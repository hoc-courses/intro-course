# Guess My Word

## Initialize Word to Guess

First, we're going to create a list of words from which we will randomly pick a word that the player needs to guess.

Here is the [starter project ](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=Guess%20My%20Word%20-%20Starter)that contains the list of words.

* create a variable called **word to guess** and initialize it a list of the characters from one of the words in the world-list. Use the **item \[random\] of list** block. And then use the split operator to break it up into a list of letters. having both the word to guess and the word progress both be lists of characters will make the processing easier.

## Track Word Progress and Guessed Letters

* create a variable called **word progress** and initialize it to a list containing with a space for each character in the word to guess. Display the list on the stage. When the user correctly guesses a letter, we will fill in the space with the correct character and the word progress will show our progress toward guessing the complete word.
* create a variable called **guessed letters** and initialize it to an empty list. We will add each character that is guessed to this list and tell the player when they have already guessed a character.

## Track Guess Processing - Updating Word Progress

* create a repeat until look that asks for a new guess, stores the result in a variable called **next guess**, and if the next guess is contained within the word to guess, then update the **word progress** list by replacing the space at each matching position with the next guess character.
* add say blocks to inform the player of their progress after each guess.
  * if they guess the same letter again
  * if the guess correctly a new letter
  * if they guess and it's not in the list.

## Further Enhancements

* add a max guess count and track how many incorrect guesses they have made, and exit the main loop if they reach the max guess count.
* add an outer loop that asks the player if he wants to play again after reaching max guess count, or getting all the letters correct.

## 

