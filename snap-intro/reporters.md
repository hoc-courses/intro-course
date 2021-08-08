# Reporters

Unlike the jigsaw-puzzle-piece-shaped _command_ blocks we've used until now, reporters don't carry out an action \(such as moving the sprite or displaying a speech balloon\) by themselves. Instead they _report_ a value, usually for use in another block's input slot.

These particular reporters tell you where the sprite is on the stage. As in algebra class, **x** means left-to-right position, and **y** means bottom-to-top position.

If your sprite is in the middle of the stage, drag it somewhere off-center. Then, drag an **x position** block into the scripting area and click on it. You should see a little speech balloon next to the block:![X Position
   speech balloon](https://beautyjoy.github.io/bjc-r/img/topic1/xpos-bubble.png)

Click on the gray box to the left of the **x position** block in the palette, and then look over to the stage. You will see that the value that the block would report is displayed on the stage:

![X Position block&apos;s checkbox](https://beautyjoy.github.io/bjc-r/img/topic1/palette-checkbox.png)     ![X Position stage
   watcher](https://beautyjoy.github.io/bjc-r/img/topic1/watcher.png)

This on-stage display is called a _watcher_.

The ![X Position
   Sensor Block](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_xposition.png) and the ![Y Position
   Sensor Block](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_yposition.png) will tell you the position of your sprite on the screen. Move the sprite around and the values reported by these blocks change.

