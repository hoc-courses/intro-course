# Simple Predicates - Comparison Operators

## Booleans

In order to represent the yes/no nature of condition phrases, we need a special type of value called a Boolean \(named after the great logician [George Boole](http://en.wikipedia.org/wiki/George_Boole)\). There are only two possible boolean values: `true` and `false` \(which correspond to "yes" and "no"\). These are represented in Snap_!_ by the blocks: ![](../.gitbook/assets/image%20%28194%29.png) and ![](../.gitbook/assets/image%20%28193%29.png).

Blocks that report `true` or `false` are called **predicates**. 

![5 &amp;gt; 3 returns &apos;true&apos;](https://beautyjoy.github.io/bjc-r/img/cond/predicate-returning-boolean.gif)

These functions are used to represent yes/no questions. Predicate functions in Snap_!_ will always have the pointed, hexagonal shape \(like this: ![a predicate block](https://beautyjoy.github.io/bjc-r/img/cond/demo-predicate-block.png)\).

## Simple Predicates - Comparison Operators

Here are a few simple predicates that are built in to Snap_!_ Most of these can be found on the green "operators" tab:

 ![](../.gitbook/assets/image%20%2885%29.png) and ![](../.gitbook/assets/image%20%2882%29.png) 

## Extra Challenge - Predicates Experiment

Read this script carefully, and make sure you understand why it produces this picture on the stage:

  
![clear
pen up
forever {
    go to \(random position\)
    if \(x position &amp;lt; y position\) {
        set pen color to purple
    } else {
        set pen color to orange
    }
    make a point
}](https://bjc.edc.org/bjc-r/img/2-complexity/dotscript.png) ![ Imagine a 45-degree line sloping upward toward the right, through the center of the stage. The area up and to the left of this line is purple; the area below and to the right is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/y-gtr-x.png)

Changing the predicate in the `if` block changes the picture. Discuss why the predicate![\(x position &amp;gt; 0\) and \(distance to apple &amp;gt; 100\)](https://bjc.edc.org/bjc-r/img/2-complexity/apple-script.png) generates this picture:

  
![There&apos;s an apple in the center. The entire left half of the stage is orange; so is a circle around the apple. What&apos;s left is purple.](https://bjc.edc.org/bjc-r/img/2-complexity/apple.png)

Match the predicate with the pictures. There are more expressions than pictures.

![](../.gitbook/assets/image%20%2828%29.png)

