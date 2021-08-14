# Drawing Polygons Project

## **Refactoring - Create a Draw Polygon Command Block**

From our earlier work we have several scripts that perform very similar instructions.

* Equilateral Triangle
* Pentagon
* Hexagon
* Octagon

Due to the nature of how the exterior angles of a regular polygon add up to 360 degrees, we can calculate the amount of rotation for any regular polygon by dividing 360 by the number of sides.

![](../.gitbook/assets/image%20%28307%29.png)

**Refactoring** is when you take some code that is functionally correct and modify/replace it to do the same task more efficiently. For this exercise, we're going to create a new command block that will draw any regular polygon and replace the ones we have built so far.

Create a command block in the **motion** palette, named **draw polygon**, that will draw all of the shapes above. It should accept two inputs:

* **sides**: the number of sides
* **length**: the length of each side

Create titles for the input parameters so that it is easier to use them.

![](../.gitbook/assets/image%20%28317%29.png)

## **Create Art**

To use our new drawing blocks we're going to create some interesting art work. One more command block will be useful before we start.

**Create a Draw Rectangle Command Block**

Create a command block in the **motion** palette, named **draw rectangle**, that will draw a rectangle with the specified width and length.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-rect.png?raw=true)

#### Prepare for Drawing

In the scripting area, set out a collection of the tools and blocks that may be handy in creating your art work. You can adjust the input values for these blocks as needed as you create your art. This [video](https://www.youtube.com/embed/pthWazhu474?rel=0) shows how to create some overlapping regions and then fill some of them with color.

![](https://github.com/hoc-labs/images/blob/main/poly-video.png?raw=true)

Make your own art. Explore a few different combinations of shape and color. Take screen shots of your art work and save them so you can share them with the class.

## Going Further

### Random Shapes

To add some randomness to your drawings try using the[ random reporter ](random-block.md)in your calls to your shape commands:

![](../.gitbook/assets/image%20%28326%29.png)

Here are some ideas:

_\*\*\*\*_![](https://github.com/hoc-labs/images/blob/main/random-polys-2.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-3.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-4.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/just-reds.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/AbstractArtReflect.png?raw=true) 

### Extra Challenge - Nested Squares

Build a **nest squares** block that uses a **for loop** block and your **draw square** block to draw nested squares. 

Give it the following input parameters:

* num squares: how many squares to draw
* initial length: the starting size of the squares
* increase: how much to increase the size of the square on each iteration

![](https://github.com/hoc-labs/images/blob/main/concentric-squares.png?raw=true)

Extend it to fill the squares:

![](../.gitbook/assets/image%20%28313%29.png)

## Resources

#### Some interesting drawing projects

* [Art Horns](https://snap.berkeley.edu/snap/snap.html#present:Username=bh&ProjectName=art-horns&editMode&noRun)
* [Filography](https://snap.berkeley.edu/snap/snap.html#present:Username=xleroy&ProjectName=19-filography&editMode&noRun)
* [BridgetRiley](https://snap.berkeley.edu/snap/snap.html#present:Username=uoc_tpi&ProjectName=BridgetRiley_&editMode&noRun)

#### A lesson describing how angles sum to 360 degrees.

{% embed url="https://youtu.be/qLU3PtaG3ww" %}



