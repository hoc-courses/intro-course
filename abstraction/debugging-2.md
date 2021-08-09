# Debugging - Part 2

The code contained in [this file](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/debugging/house-buggy) is supposed to draw a house, but something is wrong. See if you can figure out what the problem is and try to fix it so that the ![](../.gitbook/assets/image%20%28133%29.png) draws a proper house as shown below.

![](../.gitbook/assets/image%20%28235%29.png) 

## The Check Block

What happens, however, if our code does not give us a visual representation of our output \(such as a picture of a house\) and we are receiving wrong results? These cases can be a bit trickier to debug yet there are tools at our disposal. Enter the Check Block: ![](../.gitbook/assets/image%20%28194%29.png) 

**You must import tools to access the check block.** To do this, go to the dogeared page icon in the top left &gt; Libraries &gt; Iteration, Composition. Then click import, and this block will show up under the Control tab in Snap! This block works by first evaluating the predicate block passed into the diamond shaped slot, which will return either a true or false value. 

If this predicate returns true then the check block executes the commands within the C-shaped area and then pauses all of the scripts currently running. To un-pause these scripts click on the yellow button at the top right of your screen \( ![](../.gitbook/assets/image%20%2872%29.png) \). Pictured below is an easy example of how you can use the check block to debug your code:

![](../.gitbook/assets/image%20%28195%29.png)

![](../.gitbook/assets/image%20%2872%29.png)

This script should look familiar to you as it is in fact identical to a buggy version of ![sum of nums in range](https://beautyjoy.github.io/bjc-r/img/blocks/sum-of-numbers-between-1-and-10.png). Notice that the check block will pause the script if it detects that we have gone through more than one cycle of the loop \(![i greater than 1](https://beautyjoy.github.io/bjc-r/img/blocks/i-greater-than-1.png)\) but the sum has not become greater than two \(![sum not greater than 1](https://beautyjoy.github.io/bjc-r/img/blocks/not-sum-greater-2.png)\). We would expect that after going through the loop twice the sum variable should be at least three \(1 + 2\). Try running this script to see what happens \(click on the picture to go to the code\). You should notice that the sum variable shows on the stage and that its value is set to two, not three or more as expected. As such by using the check block we can conclude that there is something wrong with how we are changing the value of our sum. This might then lead us to realize that we have a set block within in the loop instead of a change block enabling us to correct the problem.

