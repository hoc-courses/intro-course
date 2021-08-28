# Bug on a Plate

Click [here ](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Starter)for starter project.

## Move Bug Around on Stage

**Step 1 -** **Respond to left, right, up and down arrows.** 

For example, here is the event handler for the left-arrow key being pressed:  ![](.gitbook/assets/image%20%28392%29.png) You will need to make sure that the bug is not moving beyond the boundary of the stage. For example, if the left-arrow is clicked, then the bug should only move if the bug's x-position is greater than then left edge of the main playing area \(have to take into account the left margin that has the game stats\).

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

## Top Score

We're going to add the capability to our game to display the top score across several games. We'll display it in the upper right corner.

![](.gitbook/assets/image%20%28389%29.png)

* Create a variable of type list, called scores, to keep all of the scores for each game as they are played.
* Create a variable, called top score, to keep the top score across multiple runs of the game. This is just clicking the "Click to Start" button multiple times, not the Green Flag.
* Display the top score variable in the upper right of the stage.
* Each time after the countdown timer runs out, add the current score to the list of scores.
* Create a reporter, called max, that returns the max of two numbers.
* Use the **max** reporter and the **combine** block to get the max score out of the scores list.
* Assign the max score to the top score variable.

## Extra Challenge

* have the bug draw a trail as it crawls and if it crosses the trail it gets a point subtracted.
* add the dustbin sprite to the left and allow the user to click it three times to erase the trail.

### Solutions

Try not to look at the solutions before working through as much as you can on your own.

* [Moving bug on stage](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%201%20-%20Move%20Bug%20on%20Stage)
* [Move fruit to new location on hit](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%202%20-%20Move%20Fruit%20on%20Hit)
* [Keeping score](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%203%20-%20Keep%20Score)
* [Countdown timer](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%204%20-%20Keep%20Time)
* [Game state](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%205%20-%20Game%20is%20Running)
* [Top Score](https://snap.berkeley.edu/snap/snap.html#present:Username=annechinn&ProjectName=BugOnAPlate%20-%20Step%206%20-%20Top%20Scores)

