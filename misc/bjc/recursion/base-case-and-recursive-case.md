# Base Case and Recursive Case

For our `tree` block, we're going to point out various parts of the anatomy of a recursive procedure. The line numbers mentioned below refer to the picture at the end of this page.  


* We always need a way to figure out that we're done and shouldn't call the recursive call again. Lines 2-4 are the _Base Case,_ in which we handle a situation so simple that we don't need to call the block recursively.
* If this isn't the base case we think to ourselves "Woah — That seems complicated. I'll just do a small part of the problem and delegate to someone else". Here's what we do: 
  * draw the trunk of the tree \(line 6\), 
  * position the sprite for the left sub-tree \(line 7\), 
  * delegate to another copy of the tree block the drawing of the left sub-tree \(line 8\),
  * re-position the sprite for the right sub-tree \(line 9\),
  * delegate to another copy of the tree block the drawing of the right sub-tree \(line 10\),
  * re-position the sprite to retrace the trunk \(line 11\), and 
  * retrace the trunk and leave the sprite exactly where it started out \(line 12\).
* Lines 6-12 are the _Recursive Case,_ in which the block calls itself using recursion.
* The _Recursive Case_ also has to work _towards_ the base case. This means that some input or other aspect of the recursive calls in the _Recursive Case_ has to be changing such that the _Base Case_ is eventually called. For our `tree` block, we are subtracting 1 from the `level` input of each recursive call, so that eventually the `level` input will reach a value of 1, which is the condition for our _Base Case_. If we cannot reach our _Base Case_, our block will keep recursively calling itself forever, getting stuck in what we call an _infinite loop_. This is what happened with our `tree` block before we modified it.

![tree with base case](https://beautyjoy.github.io/bjc-r/img/lab-10/tree-with-base-case-snap.png)

Questions:

1. What would happen if we ran our `tree` block with a `level` input of less than 1? Think about it before you try it out.

2. Sometimes you can make a recursive procedure more elegant by having a smaller base case. In our `tree` program, what would a "zero level" tree mean? Try rewriting `tree` so that the base case is `level=0`.

