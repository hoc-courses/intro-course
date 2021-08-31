# Guess My Word

## Initialize Word to Guess

First, we're going to create a list of words from which we will randomly pick a word that the player needs to guess.

Here is the [starter project ](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=Guess%20My%20Word%20-%20Starter)that contains the list of words.

Create a global variable called **word to guess** and initialize it to contain the list of the characters from one of the words in the world-list. 

Use the **item \[random\] of list** block to pick the word from the word list. Then use the **split** operator to split the word into a list of letters \(split returns a list\).

![](../.gitbook/assets/image%20%28395%29.png)

## Track Word Progress and Guessed Letters

Create a variable called **word progress** and initialize it to a list. We want to initialize it so that it is the same length as the **word to guess** list, but contains a space character, instead of the actual letter, in each place. 

Display the list on the stage. When the user correctly guesses a letter, we will fill in the space with the correct character and the word progress will show our progress toward guessing the complete word.

![](../.gitbook/assets/image%20%28400%29.png)



Create a variable called **guessed letters** and initialize it to an empty list. We will add each character that is guessed to this list and tell the player when they have already guessed a character.

![](../.gitbook/assets/image%20%28397%29.png)

## Track Guess Processing - Updating Word Progress

Create a **repeat until** block that asks for a new guess, stores the result in a variable called **guess**, and if **guess** is contained within the **word to guess**, then update the **word progress** list by replacing the space at each matching position with the next guess character.

![](../.gitbook/assets/image%20%28399%29.png)

Add say blocks to inform the player of their progress after each guess.

* if they guess the same letter again
* if the guess correctly a new letter
* if they guess and it's not in the list.

![](../.gitbook/assets/image%20%28398%29.png)

## Further Enhancements

* add a max guess count and track how many incorrect guesses they have made, and exit the main loop if they reach the max guess count.
* add an outer loop that asks the player if he wants to play again after reaching max guess count, or getting all the letters correct.

## 

