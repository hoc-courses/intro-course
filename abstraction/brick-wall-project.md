# Brick Wall Project

You are going to draw this brick wall:

![Sample image of brick wall](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/wall.png)

### Abstraction

In this problem, you will build an abstraction for drawing a brick wall, first by creating ![draw-brick](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick.png), then blocks for drawing rows, and ultimately the goal: ![draw-brick-wall-n](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-num.png).

### Level 3: Drawing One Brick \(bottom layer of abstraction\)

A brick is a solid red rectangle \("brick red," i.e., not a bright primary-color red but somewhat darker\). There's no "draw rectangle" block in Snap_!_, but we can fake it by thinking of a rectangle as a very thick line. You know how to draw a line, with the **move** block. In the **Pen** palette there's a **set pen size** block. W can use it to draw a thick line:

![](../.gitbook/assets/image%20%28379%29.png)

If you try out this code, you'll notice that your brick has rounded ends. These ends stick out beyond the length of the line you asked to draw. Here's a picture of the rounded brick with a regular line \(pen size 1\) inside it: ![](../.gitbook/assets/image%20%28380%29.png) 

For this project you're going to turn off the rounded ends. Click on the settings button \(![settings button](https://beautyjoy.github.io/bjc-r/img/sys/settings.png)\) in the toolbar, and turn on the "**Flat line ends**" setting.

You need to build the following blocks:

* **Draw Brick:** which draws a single brick. 
* **Draw Small Brick:** which draws the small brick for the edges of row B. Note that this brick will not be exactly half as long as the full brick. Part of this assignment is figuring out how long the “small brick” should be. 
* **Draw Mortar:** which draws a space between each brick or small brick.

### **Level 2: Drawing Rows: \(middle level of abstraction\)** 

A quick observation shows that there are two kinds of rows of bricks:

* **Row A**: ![Row A](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/row-a.png)
* **Row B**: ![Row B](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/row-b.png)

You can use the blocks that you built for Level1 to implement these two blocks.

### **Level 3: Drawing a Brick Wall: \(top level of abstraction\)** 

* This level of abstraction contains only the **Draw a Brick Wall with \_\_ rows** block, which draws a brick wall with the specified number of rows. 

![draw-brick-wall-7](https://beautyjoy.github.io/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-7.png)

* This function will put together the full brick wall using only the functionality provided by the middle level of abstraction, **Level 2**. So it will use **Row A** and **Row B**.

**HINT**: As you iterate through each of the rows, you will need to determine which ones should call Row A and which ones should call Row B. You can do this by determining whether the current row is an even or an odd numbered row. You can build a predicate reporter called even? that will use the mod operator to determine if a number is even or odd

### Extra  Challenge

After you've drawn the picture at the top of this page, add more inputs to the **Draw a Brick Wall** block:

* Length of the wall \(how many bricks\)
* Length of a brick
* Mortar thickness

Add these one at a time, not all at once! When you modify the length of a brick, that should also change the length of a half-brick. When you modify the mortar thickness, that should also change the distance between rows \(since that's mortar too\).

