# Random Block

We can generate a random number between any two whole numbers using the `random` block:![Random](https://beautyjoy.github.io/bjc-r/img/blocks/pick-random-1-to-10.png)

This block generates numbers with about equal likelihood, and can generate the both the lower and upper bounds that you give it. So, ![pick random](https://beautyjoy.github.io/bjc-r/img/blocks/pick-random-1-to-10.png) can generate 1, 2, 3, 4, 5, 6, 7, 8, 9, and 10.

This block \(and others with round edges\) is a **reporter** block—it _reports_ a value. Use this block inside other blocks that take an input:![Random Everywhere](https://beautyjoy.github.io/bjc-r/img/prog/pick-random-block-inside-various-blocks.png)

[This program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/random/six-sided-die.xml) simulates a six sided die that rolls every time you click on it. \(You can look in the `Costumes` area—click the tab above the script—to see the six costumes that the random number is using\).

## Randomly Moving a Character

Make a sprite keep moving around the screen randomly, using ![pick random](https://beautyjoy.github.io/bjc-r/img/blocks/pick-random-empty-args.png) blocks \(with the correct inputs\) inside ![turn right block](https://beautyjoy.github.io/bjc-r/img/blocks/turn-right.png) and ![move to](https://beautyjoy.github.io/bjc-r/img/blocks/move.png) blocks. Some things to keep track of:

* You'll want to use a ![repeat block](https://beautyjoy.github.io/bjc-r/img/blocks/repeat.png) or ![forever block](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) to keep your sprite moving continuously.
* Make sure the sprite can travel in any direction.
* How does your sprite's actions change if you have it move a fixed, rather than random, amount each time?
* Keep the pen for your sprite down, and you'll see a two-dimensional [random walk](http://en.wikipedia.org/wiki/Random_walk).

## Check for Understanding

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/random/Test-Yourself-random.html?1&2&3&4&5&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

