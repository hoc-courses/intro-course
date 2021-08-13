# Extra Challenge

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

![](../.gitbook/assets/image%20%2832%29.png)

