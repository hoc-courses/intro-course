# For Loop

## Keeping Track of Progress Through a Loop

Repeating a part of your program is a very common practice in programming. We'll call this _looping_, and there many different blocks you can use to do it in many different ways.

The ![](../.gitbook/assets/image%20%2885%29.png) block is appropriate if you want to repeat the same behavior for... ever.  
  
The ![](../.gitbook/assets/image%20%2818%29.png) block is great if you want to loop the same behavior a certain number of times. 

Sometimes, though, you want to do _almost_ the same thing for a certain number of times, but with a slight variation. For instance:

* You want to draw 20 squares on the screen, but each a different size.
* You want to draw 100 polygons with different numbers of sides.

Many such situations can be handled by the `for` block near the bottom of the Control palette:

![](../.gitbook/assets/image%20%2829%29.png)

## The For Block

The numbers in the `for` block work as you probably think they do: the inner script is run enough times to count from the left number \(`1`\) to the right number \(`10`\). As with the `repeat` block, you can change the numbers it comes with by default to change the way the block repeats.

What's new to you here, though, is the orange oval with "`i`" in it. By using this `i`, your inner blocks can know which time through the loop they are currently on. Here's how:

The ![](../.gitbook/assets/image%20%2851%29.png) block is a _variable_ that acts like a counter. You use it any place you would use a number, and it will report the value that it currently holds.

Think of the _variable_ like a box with a name—this one has the name `i`. This box is made for you by the ![](../.gitbook/assets/image%20%2829%29.png) block, and holds a different number each time through the loop. The first time it will hold `1`, or whatever is the left number in the `for` block.

You use it by dragging ![](../.gitbook/assets/image%20%2851%29.png) from the source within the `for` block down to the slot in which you will use it.

For instance:![](https://beautyjoy.github.io/bjc-r/img/looping/for-loop-drag-i.gif)

is the equivalent of ![](../.gitbook/assets/image%20%2819%29.png) 

## Using the For Block

Click this [link ](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-squirral.xml)to load the script below in a new Snap_!_ window:

![](../.gitbook/assets/image%20%2892%29.png)

Note that we changed the name of the variable, by clicking on the orange oval _without_ dragging it.

This shape is called a "squiral" — a square spiral. Do you see why it spirals outward? The length value in the ![](https://beautyjoy.github.io/bjc-r/img/blocks/move.png) varies between repetitions.

Try changing the turning angle to other numbers: 92, 126, etc.   
  
Also, try changing the turning angle and the move length to see how close you can get to a smooth spiral:  
  
![spiral](https://beautyjoy.github.io/bjc-r/img/prog/spiral.png)

## Challenge Yourself - Nested For Loops

Predict what the following script will produce and then build the script to test your hypothesis.

![](../.gitbook/assets/image%20%2811%29.png)

