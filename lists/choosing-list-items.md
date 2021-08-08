# Choosing List Items

You've probably played Geography, the game in which one player says a place name and the next player has to name another place whose first letter is the last letter of the previous place: Newark, Kentucky, Yonkers, San Francisco, Oklahoma. Have you ever gotten stuck on the letter "A"? Oklahoma, Alabama, Asia, Alaska, America, Alameda... and so on, forever.How many states start and end with the same letter? To find out, we first need a list of all the states:

![](../.gitbook/assets/image%20%28159%29.png)

Now we want to select a subset of the states, namely the ones whose first and last letters are the same. Here's the block we use for that:

![](../.gitbook/assets/image%20%28256%29.png)

Like `map`, the `keep` block has a function as its first input. Notice, though, that this grey ring's inner boundary is hexagonal. This lets you know that you should use a predicate function, which means a function that reports `true` or `false`.We want to know whether two things are equal:

![](../.gitbook/assets/image%20%2892%29.png)

The first letter of a word is letter number 1:

![](../.gitbook/assets/image%20%28120%29.png)

\(Note that we've deleted the word "world" that Snap_!_ provides as a default value, a hint about what kind of input is expected. The input slot must be empty for our function-input notation to work.\)

Finding the last letter is a little trickier; you find the length of the text and use that number to select which letter you want:

![](../.gitbook/assets/image%20%28124%29.png)

Putting all these pieces together will give us the answer we want:

![](../.gitbook/assets/image%20%28296%29.png)

You can see from the "length: 4" in the result that there are four such states.

But if you're playing Geography, the question you really want answered is "Which states start with such-and-such a letter?" You can define a block that takes a letter as input and gives the answer to that question:

![](../.gitbook/assets/image%20%28292%29.png)

![](../.gitbook/assets/image%20%2891%29.png)

![](../.gitbook/assets/image%20%2865%29.png)

  
**Try this:**

Write an expression that will select all the words of at least five letters from a list. For example, if the words in the list are `being`, `for`, `the`, `benefit`, `of`, `mister`, and **`kite`**, then your block should choose the words `being`, `benefit`, and `mister`.

Write an expression that takes a list of mixed words and numbers, and selects just the numbers, \(Hint: Look for `is` in the Operators palette.\)

Write an expression that selects from a list of words the ones that start with a vowel. \(Hint: Use `contains` in the Variables palette.\)

