# Build a Maze

Here's a solution to our `create object` block; you'll see that we abstracted the drawing routine as its own block.

![](../.gitbook/assets/image%20%28175%29.png)

![](../.gitbook/assets/image%20%28243%29.png)

Let's add our `create object` block to the end of our click detector script, so that whenever we click the board, it adds a Bug at that tile!

![](../.gitbook/assets/image%20%2836%29.png)

#### Putting It All Together!

Let's create a customizable, playable maze! Our final product will look something like this:

![](../.gitbook/assets/image%20%2865%29.png)

Head over to our Player sprite, and let's see how it works.

When the Green Flag is pressed, our player gets a position as a \(row, column\) coodinate. Notice that we have some arrow-key receivers set up- almost! When we press an arrow key, we want `position` to change accordingly. Take a look in `finish move` to see how we update the player's displayed position before we move on.

Let's fill in the arrow key receivers so that they change our position coordinate \(which is a list of two values\) appropriately. You can use the following blocks to get the "row" and "column" numbers out of the `position` variable, or you can just use "item 1" and "item 2"!

![](../.gitbook/assets/image%20%2887%29.png)

![](../.gitbook/assets/image%20%28141%29.png)

Head to the `Player` sprite, and fill in the empty lists in the arrow key receivers with the appropriate code for changing the player's position.

The last thing we have to do is add a game over condition when we hit an obstacle. When does it make sense to check to see if the game should be over? `finish move` seems like a good place, because it gets run after every move.

Fill in the `finish move` block so that it checks to see if any objects are at our `position` on the Board. Some ideas for inside the condition: Turn the sprite red; speak the words "Game over!"; have our Player say "Oops, I hit a \(object name\)!"; Reset a timer when the flag is clicked and stop it when the game is over.

Add a condition to `finish move` that checks the players `position` against the board, and do something if there's an object there!

#### Avoiding "if touching"

There's a big advantage to using boards to store info about our game state that we haven't discussed yet. And that is: using "if touching" under "sensing" is really slow.

Sometimes it's tempting to use several ![](../.gitbook/assets/image%20%28138%29.png) to check if the `Player` sprite itself is touching another object or color on the stage. Sometimes it's useful to use one of these, but in general, they're **really slow!**

Imagine if instead of moving in discrete steps and checking the item on the board at our position, we had a separate "forever if touching" script for each type of object we want to detect! This lead to repetitive code, AND each "forever if touching" really eats away at our speed.

Board representations can make games much more playable by allowing us to avoid all of this!

