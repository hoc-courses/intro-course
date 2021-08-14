# Composition of Blocks

You can treat your custom-made blocks like any other block in snap, including using them within other block you define. In fact, bigger programming tasks are usually best solved by writing simple blocks that are used within slightly more complicated blocks, which are in turn used in even more complicated blocks, and so on.

We'll look more closely at this sort of composition of blocks in a later topic, because it is important.

For now, use the ![](../.gitbook/assets/image%20%28157%29.png) block to create a block that draws the petals of a flower, like:

![](../.gitbook/assets/image%20%28295%29.png)

If you look at this flower, you'll see it has 6 squares drawn at equal angles around a full 360-degree rotation.

Create the block ![](../.gitbook/assets/image%20%28120%29.png) that will draw a square-leaved flower with any number of square-shaped petals with the specified size. In this block, you will turn the sprite between calls to `draw square`using an angle of ![](../.gitbook/assets/image%20%28270%29.png) . 

An invocation of ![](../.gitbook/assets/image%20%2898%29.png) should draw the example picture above.

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/functions/intro/buggy-house-and-square.html?1&2&3&4&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Compose a _draw flower_ Block

Write a block that draws a full flower in the middle of the stage.

![](../.gitbook/assets/image%20%28158%29.png)

Write simple custom blocks, or borrow from blocks you have already written, and then use those blocks inside your `draw a flower` block. If you can, write blocks of intermediate complexity that use and are used by other blocks you write.  
  
You might write:  
  
     `draw flower head with ...`  
  
     `draw stem with length []`  
  
but don't feel constrained by this list.

Use several inputs that control aspects of what the flower should look like. You might change the number of petals, the size of the petals, the shape of the petals or the color.



