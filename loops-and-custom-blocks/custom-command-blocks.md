# Custom Command Blocks

{% hint style="info" %}
#### Command blocks perform an action but do not return a value.
{% endhint %}

We are going to teach the computer how to draw a square using a block named `draw square`. Please follow the steps below:

Click on `make a block` at the bottom of the `Variables` palette \(or right-click or control-click on the scripting area background and choose "`make a block`"\).![&apos;make a block&apos;](https://beautyjoy.github.io/bjc-r/img/sys/MakeABlock-BYOB.jpg)

This will open up the `Make a block` dialog box. There are several steps that you'll do here, corresponding to each area of the dialog. Now, you get to choose which tab the block should go into. Our block is going to draw a square, so let us choose `Motion`. \(Note: A very common mistake is to omit this step. If you do forget, your block will become a gray Other block, in the Variables palette.\)

![&apos;make a block&apos; dialog box](https://beautyjoy.github.io/bjc-r/img/sys/make-a-block-BYOB.png)

First, at the top of the dialog, you should select in which palette the block will be place. This block is going to draw a square, so choose `Motion`. The `Motion` tab should highlight in blue, as in the picture below.

Second, you'll want to enter a title for the block in the edit field. Type `draw square`, which should show up as in the picture below.

Third, you have the option of making blocks of different shapes, corresponding to the `Command`, `Reporter`, and `Predicate` icons. By default the `Command` icon is selected, and this is the one you want. \(You will learn about the other shapes of custom blocks in the next topic\).

Fourth, there are two radio buttons that you can safely ignore. You will almost always want to keep `for all sprites` selected in this course.

![Make a command block](https://beautyjoy.github.io/bjc-r/img/sys/make-draw-square-block.png)

Click `OK`.

After you click `OK`, a dialog titled `Block Editor` will appear.

![Block Editor for &apos;draw square&apos;](https://beautyjoy.github.io/bjc-r/img/prog/empty-draw-square-BYOB.png)

Inside the you will see a specially shaped block with the title of the custom block that you are creating. This kind of block is called a "hat" block, and it indicates a starting place for the `draw square` script.

You can treat this dialog like you do the scripting area of the main Snap_!_ window. Drag blocks here from the palette to define the script that will run when your custom block is used.

1. Use the blocks from the Control and Motion palettes to create a script that draws a square, as shown below.![Script to draw a square](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-no-arguments.png)
2. When you click `OK`, you should be able to use this block as if it were a regular block. Since you created the block as a `Motion` block, it will end up at the bottom of the `Motion` tab.![Using the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/prog/draw-square-block-BYOB.gif)

Congratulations! You have just created your first custom block.

## Adding an Input 

You have created a block that draws a square, but only a square in which each side is of length `100` steps. It would be better if you could specify how long you wanted each side to be.

Edit the block to accept an _input_ \(or _argument_\), which tells it the length of the square it has to draw:

Right-click or control-click on the new block \(either in the palette or in a script\) and select `edit` to go back to the block editor.![Editing the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/edit-current-block.png)

In the `Block Editor`, hover your cursor over the words and plus signs \(**`+`**\) in the top block. \(This top block is called a "hat" block because of the curved top. Hat blocks can never be in the middle of a script, only at the top\).

Clicking on a word will let you change that word; clicking on a **`+`** will let you add something in that position. We want to add an input at the end of the block, so clickon the **`+`** at the end.

![draw square editor](https://beautyjoy.github.io/bjc-r/img/sys/draw-square-block-editor.png)

You should get the following dialog box.![Adding an argument to the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/add-argument-in-block-signature.png)

You have two choices about what you want to add or modify to the block definition:

1. `Title text` \(unselected in the picture above\) will let you add a word or words to the block's title. For example, if you wanted to change the name of the block from `draw square` to `draw square picture` you'd click on 'Title text' and type the word "picture" into the text box.
2. `Input name` \(selected in the picture above\) will let you add an input. This is the choice we want here, and will by default be selected when you open this dialog.

We want to add an input named `size` to our block definition. Type "size" in the input field and click `OK` \(since `Input name` is selected already\).

Your block title has changed: there is now a variable named `size` at the end of the title.![New variable in the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-unused-argument.png)

In order to use the `size` variable within the `draw square` block, drag the variable `size` down into the move block. Whenever you need a new copy of a variable, just drag another down. \(If you have extra copies you want to get rid of, you can drag the copy all the way to the palette at the left of the Snap_!_ window.\)  
  
Snap_!_ will determine the value of the `size` variable automatically for you whenever you use the `draw square` block in a program.![Adding a variable to the body](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-pull-argument.gif)

When you click `OK`, you'll see that the `draw square` block in the scripting area now takes an argument. You can put different numbers in the blank and draw squares of different sizes.

![Running the &apos;draw square&apos; block with an argument](https://beautyjoy.github.io/bjc-r/img/prog/draw-square-block-with-arg-BYOB.gif)

