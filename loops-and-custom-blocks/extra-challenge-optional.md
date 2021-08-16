# Geometric Designs \(Optional\)

Write the code to draw the geometric design shown below.

![](../.gitbook/assets/image%20%28353%29.png) 

You can watch this animation to get some ideas.

![](https://bjc.edc.org/bjc-r/img/1-introduction/Daisy_img/DaisyAnimation.gif)

The entire design is made up of circles. So the first thing to do is to write code that will create a circle. To do this, create a custom block `Draw Circle` via the “Variables” menu “Make a block” option. Hint: A regular polygon with 30 or more sides is a good approximation for a circle.

Now that you can draw a circle, you can generate the Daisy Design by rotating your sprite a bit at the end of each circle drawn. In the design above there are 24 circles. How much must the sprite turn each time a circle is drawn in order to make a full cycle of 360° when all the circles are drawn? Create a custom block `Draw Daisy` to do this.

Extend it further to create these patterns:

![](../.gitbook/assets/image%20%28355%29.png) ![](../.gitbook/assets/image%20%28363%29.png) ![](../.gitbook/assets/image%20%28354%29.png) ![](../.gitbook/assets/image%20%28360%29.png) 

