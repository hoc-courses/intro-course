# Brick Wall Project

You are going to draw this brick wall:

![Sample image of brick wall](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/wall.png)

### Abstraction

While Snap_!_ has lots of blocks for drawing and moving, it doesn't have anything about bricks. It wouldn't make sense to have one in general because most programs don't involve bricks. But ones that do could really use a ![draw-brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick.png) block. ![draw-brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick.png) moves us away from having to talk in the computer's terms and closer to using the terms of the problem we're trying to solve. The process of moving from what the programming language gives you to a natural language \(one that humans speak to communicate \) is critical to a good abstraction.

In this problem, you will build an abstraction for drawing a brick wall, first by creating ![draw-brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick.png), then blocks for drawing rows, and ultimately the goal: ![draw-brick-wall-n](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-num.png).

### Drawing One Brick

A brick is a solid red rectangle \("brick red," i.e., not a bright primary-color red but somewhat darker\). There's no "draw rectangle" block in Snap_!_, but we can fake it by thinking of a rectangle as a very thick line. You know how to draw a line, with the **move** block. In the **Pen** palette there's a **set pen size** block. W can use it to draw a thick line:

![Code for draw brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick-code.png)

If you try out this block, you'll notice that your brick has rounded ends. These ends stick out beyond the length of the line you asked to draw. Here's a picture of the rounded brick with a regular line \(pen size 1\) inside it:![Round brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/round-brick.png)

These rounded ends are very pretty when drawing most pictures, but they don't look like bricks, and they make thinking about lengths in this project too complicated. So for this project you're going to turn off the rounded ends. Click on the settings button \(![settings button](https://beautyjoy.github.io/bjc-r/img/sys/settings.png)\) in the toolbar, and turn on the "**Flat line ends**" setting.

### Using Problem Decomposition to Write an Abstraction

Consider this line of code that was used to create the brick wall:

![draw-brick-wall-7](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-7.png)

If you were to ask a mason to make a brick wall with seven rows, he would surely understand your meaning and make it happen. A computer, however, doesn't know what that means, so you have to fill in the details. This means going from the abstract \(draw a brick wall\) to the concrete, which involves problem decomposition.

A quick observation shows that there are two kinds of rows of bricks:

* **Row A**: ![Row A](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/row-a.png)
* **Row B**: ![Row B](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/row-b.png)

**At the lowest level of abstraction \(Level 3\):** 

* You need to figure out how to draw individual bricks, small bricks and spaces. The bricks are simply thick lines.
* This level of abstraction contains the following blocks: 
* The **Draw Brick** block, which draws a single brick. 
* The **Draw Small Brick** block, which draws the small brick for the edges of row B. Note that this brick will not be exactly half as long as the full brick. Part of this assignment is figuring out how long the “small brick” should be. 
* The **Draw Space** block, which draws a space between each brick or small brick.

**At the middle level of abstraction \(Level 2\):** 

* You can use the functionality provided by the bottom level of abstraction to make entire rows of bricks. 
* The rows referred to as “Row A” and “Row B” should look like the rows shown above. 
* This level of abstraction contains the following blocks: 
* The **Initialize Pen** block, which should initialize the pen color and size.
*  The **Initialize Character Position and Direction** block, which should initialize the position and direction of the character. 
* The **Draw Row A** block, which should draw a single copy of Row A. 
* The **Draw Row B** block, which should draw a single copy of Row B. 
* The **Transition between Row A and B with space** block, which should transition between the end of Row A and the beginning of Row B, leaving a space as wide as the number of pixels specified by the input argument. 

**HINT**: You will need to determine if there is an even number of rows or an odd number of rows to be drawn as well as if the row being drawn is an even number or odd number one. You can use the `mod` block to help.

**At the highest level of abstraction \(level 1\) :**

* You will put together the full brick wall using only the functionality provided by the middle level of abstraction. 
* This level of abstraction contains only the **Draw a Brick Wall with \_\_ rows** block, which draws a brick wall with the specified number of rows. 

In summary, you should implement the following blocks:

![](../.gitbook/assets/image%20%28365%29.png)

Note: Whenever you need to refer to a number in the program, use a variable. This is generally considered good style, because you can use the same variable in multiple places in your program, and you only need to change the value of the variable to change it in multiple places at once.

### Extra  Challenge

After you've drawn the picture at the top of this page, add more inputs to the **Draw a Brick Wall** block:

* Length of the wall \(how many bricks\)
* Length of a brick
* Mortar thickness

Add these one at a time, not all at once! When you modify the length of a brick, that should also change the length of a half-brick. When you modify the mortar thickness, that should also change the distance between rows \(since that's mortar too\).

