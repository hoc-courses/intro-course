# Drawing Polygons Project

## **Refactoring - Create a Draw Polygon Command Block**

Now we have several commands that perform very similar instructions. Due to the nature of how the exterior angles of a regular polygon add up to 360 degrees, we can calculate the amount of rotation for any regular polygon by dividing 360 by the number of sides.

![](../.gitbook/assets/image%20%2858%29.png)

**Refactoring** is when you take some code that is functionally correct and modify/replace it to do the same task more efficiently. For this exercise, we're going to create a new command block that will draw any regular polygon and replace the ones we have built so far.

Create a command block in the **motion** palette, named **draw polygon**, that will draw all of the shapes above. It should accept to inputs:

* the number of sides
* the length of each side

Create titles for the input parameters so that it is easier to use them.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-polygon.png?raw=true)

## **Create Art**

To use our new drawing blocks we're going to create some interesting art work. One more command block will be useful before we start.

**Create a Draw Rectangle Command Block**

Create a command block in the **motion** palette, named **draw rectangle**, that will draw a rectangle with the specified width and length.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-rect.png?raw=true)

#### Prepare for Drawing

In the scripting area, set out a collection of the tools and blocks that may be handy in creating your art work. You can adjust the input values for these blocks as needed as you create your art. This [video](https://www.youtube.com/embed/pthWazhu474?rel=0) shows how to create some overlapping regions and then fill some of them with color.

![](https://github.com/hoc-labs/images/blob/main/poly-video.png?raw=true)

Make your own art. Explore a few different combinations of shape and color. Take screen shots of your art work and save them to your repository and then create a web page in your  repo that displays your work so you can share them with the class.

## Going Further

To add some randomness to your drawings try using the [random reporter]() in your calls to your shape commands:

![random polygons](https://github.com/hoc-labs/images/blob/main/random-polys.png?raw=true)

Here are some ideas:

_\*\*\*\*_![](https://github.com/hoc-labs/images/blob/main/random-polys-2.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-3.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-4.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/just-reds.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/AbstractArtReflect.png?raw=true) 

## Resources

{% embed url="https://www.youtube.com/watch?v=qLU3PtaG3ww" %}

## Extra Challenge

### Nested Squares

Build a **nest squares** block that uses a **for loop** block and your **draw polygon** block to draw nested squares. Give it an input so that it will draw whatever number of squares you specify, with each square larger than the previous.

Use a **for loop** to nest squares this way. 

![](https://github.com/hoc-labs/images/blob/main/concentric-squares.png?raw=true)

Build your block with two inputs that let you specify how many squares the design will contain and how much bigger each square will be than the previous one.

### Nested Polygons

* Build a **nest polygons** block that accepts the number of polygons and the number of sides for the polygons.
* Build a script that draws 12 regular polygons, each with one more side than the previous one, as shown below.

![](https://github.com/hoc-labs/images/blob/main/polygons.png?raw=true)

