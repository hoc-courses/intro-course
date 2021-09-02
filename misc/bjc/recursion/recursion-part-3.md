# Recursion - Part 3

Last time, we tried to generalize this pattern:

![tree2](https://beautyjoy.github.io/bjc-r/img/recur/tree2.png)     ![tree3](https://beautyjoy.github.io/bjc-r/img/recur/tree3.png)     ![tree4](https://beautyjoy.github.io/bjc-r/img/recur/tree4.png)

by making a single block that took the level number as an _input,_ instead of as part of the block name:

![tree script first version](https://beautyjoy.github.io/bjc-r/img/recur/tree-nobase.png)

Unfortunately, it did not work:

![picture of failing tree](https://beautyjoy.github.io/bjc-r/img/recur/treefail.png)

The sprite draws smaller and smaller left branches, finally just spinning around in one place, without ever drawing a right branch.

What went wrong? The problem is that the original numbered `tree` scripts _aren't_ all the same. The first one, `tree1`, is different; it just draws a trunk, without any branches:

![tree1 script](https://beautyjoy.github.io/bjc-r/img/recur/tree1.png)

So our all-in-one `tree` block has to do something different from what's now in the script for the case `levels=1`.

![correct tree script](https://beautyjoy.github.io/bjc-r/img/recur/tree.png)

With this change, we can draw trees of any complexity. Here's a level-9 tree:

![picture of tree on stage](https://beautyjoy.github.io/bjc-r/img/recur/tree9.png)

\(Note: the amount of time required to draw the tree goes up very quickly with the number of levels, so we don't recommend trying 100 levels.\)

**This general code pattern, with a simple** _**base case**_ **that doesn't call the block itself, is typical of recursion. \(**_**Recursion**_ **is the name for a block that calls itself in its script.\) There's a base case and a recursive case.**

