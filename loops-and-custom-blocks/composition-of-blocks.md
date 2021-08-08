# Composition of Blocks

You can treat your custom-made blocks like any other block in snap, including using them within other block you define. In fact, bigger programming tasks are usually best solved by writing simple blocks that are used within slightly more complicated blocks, which are in turn used in even more complicated blocks, and so on.

We'll look more closely at this sort of composition of blocks in a later topic, because it is important.

For now, use the ![](https://beautyjoy.github.io/bjc-r/img/blocks/draw-square-empty-parameter.png) block to create a block that draws the petals of a flower, like:![flower with 6 square petals](https://beautyjoy.github.io/bjc-r/img/drawing/flower-with-6-square-petals.png)

If you look at this flower, you'll see it has 6 squares drawn at equal angles around a full 360-degree rotation.

Create the block  
![block: draw square-leaved flower with \[\] leaves of size \[\]](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-empty-paramters.png)  
that will draw a square-leaved flower with any number of square-shaped petals with the specified size. In this block, you will turn the sprite between calls to `draw square`using an angle of ![360 divided by the number of leaves](https://beautyjoy.github.io/bjc-r/img/drawing/calculating-turn-angle-for-draw-flower.png). 

An invocation of ![block: draw square-leaved flower with 6 leaves of size 50](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-6-50-parameters.png) should draw the example picture above.

### Test for Understanding

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/functions/intro/buggy-house-and-square.html?1&2&3&4&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Compose a draw flower Block

Write a block that draws a full flower in the middle of the stage.![draw a flower block](https://beautyjoy.github.io/bjc-r/img/drawing/draw-a-flower.png)

Write simple custom blocks, or borrow from blocks you have already written, and then use those blocks inside your `draw a flower` block. If you can, write blocks of intermediate complexity that use and are used by other blocks you write.  
  
You might write:  
  
     `draw flower head with ...`  
  
     `draw stem with length []`  
  
but don't feel constrained by this list.

Use several inputs that control aspects of what the flower should look like. You might change the number of petals, the size of the petals, the shape of the petals, or something else!

After you've worked on this for a bit, take a moment to look at what other students have done and chat. If you see something nice, spend some time trying to incorporate that design into your program.

