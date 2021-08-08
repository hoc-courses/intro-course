# Forever Loops

## Follow the Mouse

What do you think the following script will do?

![](../.gitbook/assets/image%20%28141%29.png)

**Hint**: ![](../.gitbook/assets/image%20%2822%29.png) and ![](../.gitbook/assets/image%20%28223%29.png) are reporters in the **Sensing** palette; they tell you where the mouse is pointing.

Open [the program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/follow-that-mouse.xml) \(click on the forever block to run it\). Did it follow your expectations?

Drag the mouse to a different part of the screen while the program is running and see what happens!

**Try this:** change the go to block to look like this:

![](../.gitbook/assets/image%20%2862%29.png)

How does this change the program's behavior?

## Forever Block

From the previous exercise, you may have figured out what the ![Forever block](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block does. The **forever** block is the first block you have see that holds, or wraps around, other blocks. We call this a _C block_ because of its shape. As the name **forever** implies, it will run the blocks inside it again and again and again and ... well, forever. 

![Forever And a Day Script](https://beautyjoy.github.io/bjc-r/img/intro/the-person-kept-talking-and-talking.png)

You will find this block under the **Control** tab.

Will a ![Forever block](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block ever stop?  
  
Not unless you tell it to: Click on the stop sign icon on the upper right hand corner of the Snap_!_ window.  
![Stop button](https://beautyjoy.github.io/bjc-r/img/topic1/stopbutton.png)

This stop sign will stop all scripts that are running in any sprite. This is equivalent to executing the ![stop all block](https://beautyjoy.github.io/bjc-r/img/blocks/stop-all.png) in the `Control` palette.

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/loops/forever/forever-self-test.html?1&1&2&3&topic=berkeley\_bjc%2Fintro\_pair%2F1-introduction.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Make a Kaleidoscope

Explore [this drawing program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/drawing/kaleidoscope_framework.xml) for a little bit. Press the spacebar to run the program, and move your mouse cursor over the stage of the Snap_!_ window. While over the stage, use the `d` \(pen down\), `u` \(pen up\), and `c` \(clear\) keyboard keys to change what gets drawn on the screen. The script that causes the sprite to follow the pointer is

![](../.gitbook/assets/image%20%2842%29.png)

As you can see, this drawing program features more **Control** blocks, in addition to the `forever` block first introduced in the Follow the Mouse activity. These _hat_ shaped blocks, which can be used only at the beginning of a script, indicate when a specific script should be run.

For this activity, your job is to make a \(kind of\) kaleidoscope, like:



![Kaleidoscope Activity](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_kaleidoscopegif.gif)

Some tips:

* You will need four sprites. \(We haven't used more than one sprite up to now, but having more than one allows for more interesting projects, as you'll see.\) The easiest way to create three more is to _duplicate_ the one you have. Right-click the sprite in the sprite corral, and select **duplicate** from the _context menu_ that appears. Each duplicated sprite will have exactly the same scripts as the original, which is why we suggest duplication rather than just creating more sprites from scratch.
* You can change the color of each sprite by clicking the color input in that sprite's ![](../.gitbook/assets/image%20%2843%29.png) block \(found under the **Pen** tab\), choosing a color, and then clicking on the the block itself \(to run the block and actually set the color\). Don't worry about matching the colors in the animation exactly!
* Pay close attention to what each of the other sprites is doing in the animation above. You will need to modify the **x** and **y** inputs in each sprite's ![](../.gitbook/assets/image%20%28206%29.png) block using simple formulas, with ![](../.gitbook/assets/image%20%28150%29.png) and ![](../.gitbook/assets/image%20%2840%29.png) .
* Hint: All the sprites are reflecting in different ways around the \(x=0, y=0\) origin point of the stage. \(Notice that one sprite is following the mouse.\)

Once you figured this out, try out some complicated formulas and/or more sprites, and share with your classmates!

