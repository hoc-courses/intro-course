# Project - 2048

**Reminder that you can work on 2048 in pairs.** Your partner \(if any\) that you work with in lab today does not necessarily need to be the same partner that you work with on 2048 throughout the next week and a half.  


Before beginning this lab, read over the [spec for 2048](https://docs.google.com/document/d/199V-21R31Jk0D2zigXwEEM7GIuB8Ewhff4alUh4_Cg4).

Exactly how many blocks are you supposed to implement for project 3? If you didn't answer 5,  give the spec another look! The section called **Requirements** gives a detailed overview of the required blocks for this assignment.

### Test Your Understanding

Now that you've read over the basics of the assignment, let's refine our understanding. Begin this lab by opening up the starter file linked on the assignment spec. You should see:

![](../.gitbook/assets/image%20%28279%29.png)

Click on the "Game Code" Sprite, and you should see a ton of code. **For this project, you should NOT change any existing code in this sprite \(otherwise you might break the game\),** unless you are doing some of the extra credit options.

Without changing any existing code, add a script to the scripting area of the Game Code sprite with the following code \(the "update display for" block is under Looks\). Run it, and you should see a 2 appear gloriously in the top right corner. What this code does is it first creates a new empty gameboard of size 4x4, then it places a 2 at position \(1,4\) in the gameboard \(this corresponds to the top right corner\), and lastly it updates the display of the screen so that a picture of a 2 actually appears.

![](../.gitbook/assets/image%20%2814%29.png)

**For You To Do:**

Modify the script above so that it displays the board pictured below. This is an opportunity for you to use the ![](../.gitbook/assets/image%20%2875%29.png) ****block and learn how the grid works for the 2048 game. **Note:** if you want the images to appear you will need to use the update display block after setting the appropriate values in the board \(as is shown above\).

![](../.gitbook/assets/image%20%28277%29.png)

In the above image, what is the position of the **16** tile?

* \(2, 1\) - Consider what the starting value of the left box is. Is it 0 or 1?
* \(3, 2\)
* \(2, 3\) - Remember, that we specify positions in the format \(row, column\)
* \(2, 2\) - Which corner of the board is \(1, 1\)? Start counting from there.



