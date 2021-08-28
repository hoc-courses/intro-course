# Bug on a Plate

Click [here ](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Starter)for starter project.

## Move Bug Around on Stage

**Step 1 -** **Respond to left, right, up and down arrows.** 

For example, here is the event handler for the left-arrow key being pressed:  ![](.gitbook/assets/image%20%28391%29.png) You will need to make sure that the bug is not moving beyond the boundary of the stage. For example, if the left-arrow is clicked, then the bug should only move if the bug's x-position is greater than then left edge of the main playing area \(have to take into account the left margin that has the game stats\).

* left edge: -160
* right edge: 230
* top edge: 170
* bottom edge: -170.

If it's ok to have the bug move, then call a new block that you will build named **move bug.**

**Step 2: - create move bug block.**

For the first version, just have the bug move 5 steps, and change to the next costume, which will make the bug look like it is crawling as it moves.

## Move Fruit to new Location on Hit

Go to the Fruit sprite and remove the hide command, make sure it is visible by clicking the show command, then add the following:

* a forever loop to continually check to see if the fruit is touching the bug.
* if it is, then
  * hide the fruit
  * play the "pop" sound
  * go to a random x,y position on the screen
    * x should be between -160 and 230
    * y should be between -170 and 170.
  * switch to a random costume for the sprite \(there are five costumes\)
  * show the sprite

## Keep Score

Create a global variable to track the score. 

* initialize it to zero 
* display the score on the stage on the top of the left margin  \(it will display by default, but change the view type to large\)
* increment it every time a fruit is touching the bug.

## Create a Countdown Timer

Go to the Timer sprite and remove the hide command, make sure it is visible, by clicking the show command, then add the following:

* add a global variable called countdown timer
* initialize it to 30
* display the value on the stage under the Timer sprite
* on the stage script, setup a repeat until loop that repeats until the countdown timer = 0
* on each iteration
  * wait 1 second
  * decrement the value of the countdown timer by 1
  * play the tick sound

## Keep track of Game State

The stage has two costumes. One that says "Bug on Plate" and the other that says "Click to start". We want to start off with the "Click to Start" costume, and then if the user clicks the stage when that one is active, switch to the other one, and then start the countdown timer sequence.

Once the countdown timer reaches 0, switch the costume back to "click to start".

![](.gitbook/assets/image%20%28381%29.png)

* only allow the the bug to crawl if countdown timer is greater than 0
* only allow the check to see if the fruit is touching the bug to occur if the countdown timer &gt; 0.

### Solutions

Try not to look at the solutions before working through as much as you can on your own.

* [Moving bug on stage](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%201%20-%20Move%20Bug%20on%20Stage)
* [Move fruit to new location on hit](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%202%20-%20Move%20Fruit%20on%20Hit)
* [Keeping score](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%203%20-%20Keep%20Score)
* [Countdown timer](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%204%20-%20Keep%20Time)
* [Game state](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%205%20-%20Game%20is%20Running)
* [Top Score](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%206%20-%20Top%20Scores)



