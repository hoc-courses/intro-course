# Drawing Polygons Project

## **Refactoring - Create a Draw Polygon Command Block**

From our earlier work we have several scripts that perform very similar instructions.

* Equilateral Triangle
* Pentagon
* Hexagon
* Octagon

Due to the nature of how the exterior angles of a regular polygon add up to 360 degrees, we can calculate the amount of rotation for any regular polygon by dividing 360 by the number of sides.

![](../.gitbook/assets/image%20%28368%29.png)

![](../.gitbook/assets/image%20%28307%29.png)

**Refactoring** is when you take some code that is functionally correct and modify/replace it to do the same task more efficiently. For this exercise, we're going to create a new command block that will draw any regular polygon and replace the ones we have built so far.

Create a command block in the **motion** palette, named **draw polygon**, that will draw all of the shapes above. It should accept two inputs:

* **sides**: the number of sides
* **length**: the length of each side

Create titles for the input parameters so that it is easier to use them.

![](../.gitbook/assets/image%20%28317%29.png)

## **Resources**

A lesson describing how angles sum to 360 degrees.

{% embed url="https://youtu.be/qLU3PtaG3ww" %}

