# The List Block

## Creating a List Block

Look in the Variables palette below the orange variable-related blocks for a bunch of red blocks. These blocks are about lists. A list is a way to combine several values into one grouped value.

The first red block is the `list` block, used to create a list:

![](../.gitbook/assets/image%20%28187%29.png)

Drag a `list` block into the scripting area to experiment with.

This block uses a Snap_!_ feature you've seen once before, in the `join` block: a variadic input. This means that, even though you see one input slot in the block, you can give it any number of inputs. The left and right arrowheads at the end of the block are used to delete or add input slots:

![](../.gitbook/assets/image%20%28127%29.png)

  
  
Like any reporter block, the `list` block can be dragged into an input slot of another block:

![](../.gitbook/assets/image%20%28202%29.png) ![](../.gitbook/assets/image%20%2874%29.png) 

The grey rounded rectangle with red rounded rectangles inside it is the visual representation of a list. Each red rectangle is one list item.

The list picture has several extra widgets: a + button, the downarrow, and so on. When a list value is seen in a variable watcher, you can use these controls to modify the contents of the list directly. But we're not doing that for a while, so for now just focus on the values in the red rectangles.

## Why do we Need Lists?

Let's say you're writing a program to generate English sentences. Your starting point might be various lists of words:

Click [here ](https://snap.berkeley.edu/snap/snap.html#open:https://bjc.edc.org/Sept2015/bjc-r/prog/3-lists/U3Lab1Sentence.xml)to see the script in Snap!.

![](../.gitbook/assets/image%20%28160%29.png)

You could build up a sentence out of phrases. For example, to make a noun phrase, you want to pick one item from the `articles` list, one from the `adjectives` list, and one from the `nouns` list. To select one item from a list, use the `item` block:

![](../.gitbook/assets/image%20%28256%29.png)

List items are numbered from 1, so, for example, item 3 of the `nouns` list above is `pizza`. The first input slot accepts a number like other rounded input slots, but it also has a downward arrow that, when clicked, offers two special choices: `last` for the last item of the list, and `any` to pick an item at random.

The second input slot in the `item` block is something you haven't seen before: a rectangle with two orange smaller rectangles inside it. Just as a rounded input slot indicates that a number is expected, and a hexagonal input slot indicates that a `true` or `false` value is expected, this new kind of input slot means that a list value is expected. It's meant to look like what you see when you **`say`** a list: a grey \(rounded\) rectangle with red-orange rectangles for the individual items.

Use the `item random` feature to make a noun phrase by choosing a random article, a random adjective, and a random noun:

![](../.gitbook/assets/image%20%2876%29.png)

Because of the random item choices, we get a different result each time we call `noun phrase`:

![](../.gitbook/assets/image%20%28174%29.png)

