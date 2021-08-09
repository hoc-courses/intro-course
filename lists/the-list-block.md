# The List Block

## Creating a List Block

Look in the Variables palette below the orange variable-related blocks for a bunch of red blocks. These blocks are about lists. A list is a way to combine several values into one grouped value.

The first red block is the `list` block, used to create a list:

![](../.gitbook/assets/image%20%28186%29.png)

Drag a `list` block into the scripting area to experiment with.

This block uses a Snap_!_ feature you've seen once before, in the `join` block: a variadic input. This means that, even though you see one input slot in the block, you can give it any number of inputs. The left and right arrowheads at the end of the block are used to delete or add input slots:

![](../.gitbook/assets/image%20%28127%29.png)

  
  
Like any reporter block, the `list` block can be dragged into an input slot of another block:

![](../.gitbook/assets/image%20%28201%29.png) ![](../.gitbook/assets/image%20%2874%29.png) 

The grey rounded rectangle with red rounded rectangles inside it is the visual representation of a list. Each red rectangle is one list item.

The list picture has several extra widgets: a + button, the downarrow, and so on. When a list value is seen in a variable watcher, you can use these controls to modify the contents of the list directly. But we're not doing that for a while, so for now just focus on the values in the red rectangles.  
  
**Try these:**  
What value do you get if you call the `list` block with no inputs? \(Use the left arrow to delete the original input slot.\)

Can you drag other reporters into `list` input slots to compute the list items?

What happens if you drag a `list` block into an input slot that expects a number as input, such as the inputs to the arithmetic operators?

## Why do we Need Lists?

Let's say you're writing a program to generate English sentences. Your starting point might be various lists of words:

![](../.gitbook/assets/image%20%28160%29.png)

You could build up a sentence out of phrases. For example, to make a noun phrase, you want to pick one item from the `articles` list, one from the `adjectives` list, and one from the `nouns` list. To select one item from a list, use the `item` block:

![](../.gitbook/assets/image%20%28254%29.png)

List items are numbered from 1, so, for example, item 3 of the `nouns` list above is `pizza`. The first input slot accepts a number like other rounded input slots, but it also has a downward arrow that, when clicked, offers two special choices: `last` for the last item of the list, and `any` to pick an item at random.

The second input slot in the `item` block is something you haven't seen before: a rectangle with two orange smaller rectangles inside it. Just as a rounded input slot indicates that a number is expected, and a hexagonal input slot indicates that a `true` or `false` value is expected, this new kind of input slot means that a list value is expected. It's meant to look like what you see when you **`say`** a list: a grey \(rounded\) rectangle with red-orange rectangles for the individual items.

Use the `item random` feature to make a noun phrase by choosing a random article, a random adjective, and a random noun:

![](../.gitbook/assets/image%20%2876%29.png)

Because of the random item choices, we get a different result each time we call `noun phrase`:

![](../.gitbook/assets/image%20%28173%29.png)

**Try this:**

Create blocks `prepositional phrase`, `verb phrase`, and anything else you need, ending with a `sentence` block that reports sentences like "the little elephant runs excitedly around the big pizza." Can you improve on this so that the sentence structure varies, sometimes including people's names instead of article-adjective-noun phrases, for example? You might want different sentence structures for transitive and intransitive verbs. This is an open-ended project!

Besides lists of words, you'll find uses for lists of numbers, to keep track of your grades in this course, for example, or to represent a sprite's position as a single vector \(list\) containing the X and Y position numbers. And you can even use lists of lists for more complicated data structures:

![](../.gitbook/assets/image%20%2878%29.png)

