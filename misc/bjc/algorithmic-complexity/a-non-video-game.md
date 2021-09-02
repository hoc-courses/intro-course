# A \(non-video\) Game

Let's play a number-guessing game \(you have already [seen this before](https://beautyjoy.github.io/bjc-r/cur/programming/conditionals/number-guessing-game-v2-0.html)\).  

Between your partner and yourself, decide who will be the guesser and the the picker. The picker chooses a number between 1 and 50, privately. The guesser's role is to determine what the number is, and to that end asks the picker questions with the only possible answers being "yes" or "no".

The guesser should try two different strategies to playing this game:

1. **Guessing in sequence**: "Is the number 1?", "Is the number 2?", "Is the number 3?", and so on.
2. **Guessing halfway**: You know the number must be between 1 and 50, so you start off by asking "Is the number greater than 25?". If the answer is "yes", you instantly know that it must be between 26 and 50, so you ask "Is the number greater than 37?" \(that is, halfway between 26 and 50\).  If the answer to the original question was no, the number must be between 1 and 25, so you ask "Is the number greater than 12?"

Play several times. The picker should pick a wide variety of numbers, while the guesser should use each strategy alternately.

As you play each game, think about the ways in which one strategy is better than the other. Which strategy would be better if, say, the guessing game involved numbers from 1 to 1000? From 1 to a million? From 1 to 3?  
  
Are there other strategies you can think of?

