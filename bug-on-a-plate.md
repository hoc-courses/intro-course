# Bug on a Plate

## Move Bug Around on Stage

**Step 1 -** **Respond to left, right, up and down arrows.** 

For example, here is the event handler for the left-arrow key being pressed:  ![](.gitbook/assets/image%20%28389%29.png) You will need to make sure that the bug is not moving beyond the boundary of the stage. For example, if the left-arrow is clicked, then the bug should only move if the bug's x-position is greater than then left edge of the main playing area \(have to take into account the left margin that has the game stats\).

* left edge: -160
* right edge: 230
* top edge: 170
* bottom edge: -170.

If it's ok to have the bug move, then call a new block that you will build named **move bug.**

**Step 2: - create move bug block.**

For the first version, just have the bug move 5 steps, and change to the next costume, which will make the bug look like it is crawling as it moves.

## Move Fruit to new Location on Hit

Go to the Fruit sprite and remove the hide command, then add the following:

* a forever loop to continually check to see if the fruit is touching the bug.
* if it is, then
  * hide the fruit
  * go to a random x,y position on the screen
    * x should be between -160 and 230
    * y should be between -170 and 170.
  * switch to a random costume for the sprite \(there are five costumes\)
  * show the sprite







#### **Step 1 - Move Bug around on Stage**

* **respond to left, right, up and down arrows.**
  * **if the bug is not off the stage then….**
    * **point in the new direction**
    * **call move block**
* **move block**
  * **move 4 units**
  * **change costume \(to simulate crawling\)**

