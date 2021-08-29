# Guess My Word

## Initialize Word to Guess

First, we're going to create a list of words from which we will randomly pick a word that the player needs to guess.

Here is the [starter project ](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=Guess%20My%20Word%20-%20Starter)that contains the list of words.

* create a variable called **word to guess** and initialize it a list of the characters from one of the words in the world-list. Use the **item \[random\] of list** block. And then use the split operator to break it up into a list of letters. having both the word to guess and the word progress both be lists of characters will make the processing easier.

## Track Word Progress and Guessed Letters

* create a variable called **word progress** and initialize it to a list containing with a space for each character in the word to guess. Display the list on the stage. When the user correctly guesses a letter, we will fill in the space with the correct character and the word progress will show our progress toward guessing the complete word.
* create a variable called **guessed letters** and initialize it to an empty list. We will add each character that is guessed to this list and tell the player when they have already guessed a character.

