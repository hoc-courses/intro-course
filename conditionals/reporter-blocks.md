# Reporter Blocks

So far, all of the blocks you've defined have been "command" blocks. These actual carry out an action that affects the state of the program. For example, the `move` block makes the sprite move, and the `say` block makes the sprite say something. We call these effects "side effects."

Sometimes, we aren't interested in any side effects, and just want a block that performs a calculation for us. These are called "reporters," because rather than causing the program to do something, they simply give us back a value. Many blocks on the "operators" palette are reporters. Here are just a few:

![](../.gitbook/assets/image%20%2864%29.png)

Notice how all of these are rounded, and can't be attached directly to other blocks. Because of this, we need to use them in combination with other blocks, like `say` or `set`. For example:

![](../.gitbook/assets/image%20%2858%29.png)

\(I'm sure you've been doing things like this since you started using Snap_!_\)

Let's learn how to make our own reporter blocks!

The first step is, as usual, to select "make a block" from the bottom of the "variables" palette.

Next, we'll select "reporter" rather than the usual "command."

![](../.gitbook/assets/image%20%28126%29.png)

Note: you don't have to necessarily put all reporters in the "operators" palette; it's just the most frequent place for them.

Once you give your block a name and click "OK," your block definition will look something like this:

![](../.gitbook/assets/image%20%2816%29.png)

Notice that ![report \(\)](https://beautyjoy.github.io/bjc-r/img/blocks/report.png) has automatically been added to the block definition. This is to remind you that all reporter blocks _must_ report a value.

Fill in the body with whatever you want, and you're done!

Let's take a look at an example:

![](../.gitbook/assets/image%20%2873%29.png)

This block will take in a parameter `x`, and report `x2`.

Here's a more complex example, using `if`:

![](../.gitbook/assets/image%20%284%29.png)

This block is a home-made version of the `abs` \(absolute value\) block that we saw earlier. Notice that it contains two `report` blocks. Reporter blocks can have as many `report`s as you want/need.

Let's try writing our own reporter block! Try writing a `max` block that takes in two numbers and reports the larger of the two. Hint: you'll need to use `if`.

![](../.gitbook/assets/image%20%28137%29.png)

Here's a more complex block that we wrote. Predict what it will report when run with inputs "hello" and 

![](../.gitbook/assets/image%20%28139%29.png)

"Predicates" are special kinds of reporter blocks that only report `true` or `false`. You'll see in the next slide how to write them.

