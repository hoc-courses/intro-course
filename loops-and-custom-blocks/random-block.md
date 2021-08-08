# Random Block

We can generate a random number between any two whole numbers using the `random` block:

![](../.gitbook/assets/image%20%28117%29.png)

This block generates numbers with about equal likelihood, and can generate the both the lower and upper bounds that you give it. So, ![](../.gitbook/assets/image%20%28117%29.png) can generate 1, 2, 3, 4, 5, 6, 7, 8, 9, and 10.

This block \(and others with round edges\) is a **reporter** block—it _reports_ a value. Use this block inside other blocks that take an input:

![](../.gitbook/assets/image%20%2834%29.png)

[This program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/random/six-sided-die.xml) simulates a six sided die that rolls every time you click on it. \(You can look in the `Costumes` area—click the tab above the script—to see the six costumes that the random number is using\).

## Randomly Moving a Character

Make a sprite keep moving around the screen randomly, using ![](../.gitbook/assets/image%20%28117%29.png) blocks \(with the correct inputs\) inside ![](../.gitbook/assets/image%20%28165%29.png) and ![](../.gitbook/assets/image%20%28166%29.png) blocks. Some things to keep track of:

* You'll want to use a ![](../.gitbook/assets/image%20%2830%29.png) or ![](../.gitbook/assets/image%20%28161%29.png) to keep your sprite moving continuously.
* Make sure the sprite can travel in any direction.
* How does your sprite's actions change if you have it move a fixed, rather than random, amount each time?
* Keep the pen for your sprite down, and you'll see a two-dimensional [random walk](http://en.wikipedia.org/wiki/Random_walk).

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/random/Test-Yourself-random.html?1&2&3&4&5&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Extra Challenge - Draw a Field of Flowers

Draw a field of flowers, and give each flower a different color, size, shape, position, and so forth. Use some of the simple custom blocks you've already written, and write new custom blocks that make use of those simpler blocks to do complicated things.  
  
Use ![](../.gitbook/assets/image%20%2830%29.png) to draw lots of flowers, flowers with lots of petals, and so forth.  
  
Use ![](../.gitbook/assets/image%20%28117%29.png) as much as you can to make the flowers interesting and different.

Here is a custom block \(from someone who went crazy\) to give you some ideas:

![](../.gitbook/assets/image%20%2877%29.png)

