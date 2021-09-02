# Making Your Own Board

Today we are going to make a general purpose game board! Underestanding how to make a board will give you a better understanding of the boards in Project 3

Here is the [starter file](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/lists/board_game_starter.xml) for the lab

One way to think of a board is as a collection of values at \(row, column\) coordinates. How can we represent this though when it comes to implementation? Lists store values, so let's start there.

Lists are groups of things in order, and we can group coordinates on a board into rows and columns:

![](../../../.gitbook/assets/image%20%28169%29.png)

Let's choose to think of our board as a group of rows. Notice that each row is a group of values.

![](../../../.gitbook/assets/image%20%2833%29.png)

It would make sense that each row be a list, right? The length of each list would then be the number of columns the board has. Since our board is made up of rows, it can be a list that stores all of the rows in it! Here's a visual representation of what this means:

![](../../../.gitbook/assets/image%20%28128%29.png)

In the lab file, we have already written a block called `create board of length ( )` that builds this structure for us. Check inside it to make sure we're all on the same page. For a board of size N, meaning a board with N rows and N columns, the block will generate a list with N items. Each item is a list of length N representing a row. Just like we planned!

Now that we have a board representation, we need to be able to work with it! Fill in `set () () of board` and `item () () of board` blocks so that they behave properly with our new style of board.

When you're done, congrats! You've just made your own board type.

How would our `set` and `get` blocks change if we decided to group coordinates by column instead?

