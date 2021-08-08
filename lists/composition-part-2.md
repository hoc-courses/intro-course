# Composition - Part 2

Think how much worse it would be to build the `acronym` block if we didn't have lists to help organize such tasks. You'd take the text string `phrase` and write a loop to go through it, character by character, looking for spaces as word separators. Then you'd have to build up the result string, adding one letter at a time.

![alphabet gif](https://beautyjoy.github.io/bjc-r/img/list/hof/alphabet.gif)

With `map`, `keep`, and `combine`, you can operate on the items of a list all at once. You don't have to think, "Find the first letter of the first word and operate on it, then increase the loop index until you find a space, then skip over any extra spaces that might be next to it, then remember the position of the beginning of the second word" and so on. You can think, "give me the first letters of all the words."  
  
\(Instead, all that ugliness about looking for spaces is hidden inside the `sentence->list` block, where everyone writing an application about sentences can use it without having to reinvent it. This is another example of abstraction, which we mentioned right at the beginning as one of the central ideas of the course and of computer science in general.\)

#### Try this:

Write a `longest word` block that takes in a sentence and reports the longest word.

If you get stuck on `longest word`, try making a block which reports the longer of **only 2** words and use that in your solution.

Imagine that you're writing a program to play Hangman. The program has thought of a secret word, and the user is trying to guess it. Write a `display word` block that takes two inputs, the secret word and a list of the letters guessed by the user so far. It should report the letters of the secret word, spaced out, with underscore characters replacing the letters not yet guessed:

![](../.gitbook/assets/image%20%28241%29.png)

\(Use the `word to list` block or the `split` block on the secret word to get started.\)  
In your own program, you would likely use this block within a `say` block, like this:

![](../.gitbook/assets/image%20%28294%29.png)

Consider why it's best to make the block a reporter, rather than directly `say`ing the result.

Write a reporter `exaggerate` that takes a sentence as input and reports an exaggerated version:

![](../.gitbook/assets/image%20%28126%29.png)

It should replace "good" with "great," "bad" with "terrible," "like" with "love," etc. And it should replace every number with twice the number.

