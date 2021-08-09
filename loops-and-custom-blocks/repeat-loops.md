# Repeat Loops

## Don't Repeat Yourself - let Snap! do it for you!

We can use the ![](../.gitbook/assets/image%20%2835%29.png) block to make drawing shapes a lot easier! You can see below a script to draw a square. It is, of course, much easier to create this script.

![](../.gitbook/assets/image%20%28289%29.png)

than to create this one:

![](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/move-50-turn-right-90-%284-times%29.png)

There are three different numeric values in the script—`4`, `100`, and `90`—that you can think of as parameters that change the resulting picture. Play with the [script ](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-a-square.xml)to understand how each number contributes to the "squareness" of the shape that is drawn.

### Repeat Makes Structure Clearer

Even more importantly, using `repeat` makes the _structure_ of the program clearer. This is essential to good coding. Clearly structured code is easier to understand and easier to debug \(to catch and fix errors\). In the longer script above \(without `repeat`\), we'd have to count the parts to see if it's right. And it would be very easy to make a mistake if we were drawing a 20-sided figure instead of a 4-sided one!

### Challenge Yourself

Here are four pictures.  
![Square with sides alternating red and blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/Square-alternating-red-and-blue.png) ![6-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/6-sided-figure-alternating-red-and-blue.png) ![8-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/8-sided-figure-alternating-red-and-blue.png) ![12-sided figure, sides alternating 3 red 3 blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/12-sided-figure-alternating-3-red-and-3-blue.png)  


Which one\(s\) of these pictures could be drawn by running the following script? 

![repeat 4, red move turn, blue move turn](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/non-pseudo.png)

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/intro/drawing/repeat-self-test.html?topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Drawing Regular Polygons with Repeat

![](../.gitbook/assets/image%20%28295%29.png)

A regular polygon is a shape in which all the sides are the same length and all the turning angles are the same. A square is a regular 4-sided polygon.

[![drawing a square and squiggle](https://beautyjoy.github.io/bjc-r/img/looping/drawing-regular-polygons.gif)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-square-and-squiggle.xml)

Using a ![](../.gitbook/assets/image%20%2835%29.png) to draw the following regular shapes:

* Equilateral Triangle
* Pentagon
* Hexagon
* Octagon

As you draw regular polygons with more and more sides, you are getting closer and closer to a circle. Is there a point at which is actually \(mathematically\) a circle?

If you are having trouble with determining the angle to turn, think about the direction the sprite it pointing and how far it needs to rotate when it turns.

![regular polygons](https://github.com/hoc-labs/images/blob/main/racecar.gif?raw=true)

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/intro/drawing/angles-self-test.html?1&1&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Drawing a Star

Complete the code below to draw a star.

 ![](../.gitbook/assets/image%20%28114%29.png) ![](../.gitbook/assets/image%20%28123%29.png) 

A regular star is closely related to a pentagon. And, remember, a turning angle of `72` draws a regular pentagon.

Use the `turn` block before the `repeat` block so that the star isn't drawn tilted. But, don't worry about this until you got the other `turn` block figured out.

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/intro/drawing/angles-self-test-2.html?1&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

