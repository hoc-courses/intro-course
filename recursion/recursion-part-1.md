# Recursion - Part 1

Our goal is to draw a tree like this:

![](../.gitbook/assets/image%20%28308%29.png)

but we'll start with a simpler version that shows the technique clearly, although less prettily:

![](../.gitbook/assets/image%20%2880%29.png)

The key to understanding this technique is to see that the tree is a fractal, that is, a picture that contains smaller versions of itself:

![](../.gitbook/assets/image%20%28237%29.png)

We're going to create a `tree` block in Snap_!_. It'll start with a `move` block to draw the trunk of the tree, then a `turn` block turning left, then a `tree` block to draw the left smaller tree, and so on.

"Wait!" you're probably thinking. "How can we use a `tree` block inside a `tree` block? It doesn't exist yet!" That's the big idea for this assignment.

We're going to work up to the complicated tree starting with very simple steps.

1. Make a `tree1` block \(so named because it draws just one level of the tree\) using this script:

![](../.gitbook/assets/image%20%28242%29.png)

This looks ridiculously simple, but trust us, it'll get interesting soon. When run, the script draws one tree branch, and then moves the sprite back to its original position. That's going to be really important when we start using scripts within scripts; we always want to be able to assume that our tree blocks leave the sprite in the same position and direction as it started in.

2. **Point the sprite facing upward**, and put the pen down. Then try `tree1 size 50`. You should get a result something like this:

![](../.gitbook/assets/image%20%28101%29.png)

3. Make a `tree2` block that draws two levels. Actually, you're going to make two different versions of this, so call the first one `tree2a`.

![](../.gitbook/assets/image%20%28256%29.png)

When run, it should give this result:

![](../.gitbook/assets/image%20%28249%29.png)

At this rate you'll never be able to make the beautiful version of the tree in this century. In the next step, we'll discuss how to simplify this process.  


Before going on, make sure that you can mentally trace through the code provided. Paying close attention to the forwards and turns is going to be important to see the big picture and understand the recursion.

