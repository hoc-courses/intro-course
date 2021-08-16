# Kaleidoscope

## Make a Kaleidoscope

Explore [this drawing program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/drawing/kaleidoscope_framework.xml) for a little bit. Press the spacebar to run the program, and move your mouse cursor over the stage of the Snap_!_ window. While over the stage, use the `d` \(pen down\), `u` \(pen up\), and `c` \(clear\) keyboard keys to change what gets drawn on the screen.

{% hint style="info" %}
You can also click on any of the individual blocks to get it to execute. 
{% endhint %}

The script that causes the sprite to follow the pointer is:

![](../.gitbook/assets/image%20%2843%29.png)

As you can see, this drawing program features more **Control** blocks, in addition to the `forever` block first introduced in the Follow the Mouse activity. These _hat_ shaped blocks, which can be used only at the beginning of a script, indicate when a specific script should be run.

For this activity, your job is to make a \(kind of\) kaleidoscope, that has four sprites all following your mouse movements in different patterns:



![Kaleidoscope Activity](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_kaleidoscopegif.gif)

**Some tips:**

* There are four sprites. \(We haven't used more than one sprite up to now\) 
* Pay close attention to what each of the other sprites is doing in the animation above. You will need to modify the **x** and **y** inputs in each sprite's ![](../.gitbook/assets/image%20%28215%29.png) block using simple formulas, with ![](../.gitbook/assets/image%20%28156%29.png) and ![](../.gitbook/assets/image%20%2841%29.png) .
* All the sprites are reflecting in different ways around the \(x=0, y=0\) origin point of the stage. \(Notice that one sprite is following the mouse.\)

