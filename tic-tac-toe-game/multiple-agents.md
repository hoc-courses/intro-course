# Multiple Agents

For our case, it was fine to go stamp objects on the display when we create them. Think about how we'd write a block that could delete an object from the board: we'd need to set that item on the board to 0 or 'blank', and then stamp a white or blank spot on the display to get rid of the image.

But imagine if the objects could move around too? It'd get complicated really fast- imagine trying to keep track of all of those objects with their own position variables like we did with the `Player`!

This would be a perfect case for a new type of display board, in which objects are drawn on the board according to their positions in the board, instead of according to outside variables. So if we want to move several objects on the board, we use the set block to change their positions, and then re-draw the entire board. Let's take a look at some implementations to see what we mean:

Below is our update display. Notice that every time we click it, the entire board is redrawn.

![update display block contents](../.gitbook/assets/image%20%2891%29.png)

Here's where it gets good. To draw the objects on the board, we iterate over row and column values while moving the sprite at the same time! By reading the item at the current \(row, column\) from the board, we can stamp something if needed as we go.

![draw object block contents](../.gitbook/assets/image%20%28291%29.png)

Let's make sure we know what's going on in the stamp block as well \(The "if object" is just a short way of saying "if something was there"\).

![stamp object block contents](../.gitbook/assets/image%20%2890%29.png)

Try it out if you'd like: use the `Set` block to set some bugs somewhere on the board, then run `update display`.

#### Nice Job!

That's it for this lab about boards and how to create a good one for your purposes. You may find yourself wanting to refer back to this lab when your planning your midterm project, if applicable!

