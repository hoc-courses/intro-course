# If and If-Else

Now that we have the idea of predicates under our belt, we can finally express full "if-then" statements, such as "if the weather is nice, you should go outside." This can be expressed in Snap using the ![](../.gitbook/assets/image%20%2856%29.png) block. Notice how the first slot is shaped just like a predicate block. 

`if` blocks only know how to handle yes/no questions, so you should only ever put predicate blocks into this slot. The C-shaped part of the `if` block is where you put the commands that should be run if the condition is true. Let's take a look at an example:

![](../.gitbook/assets/image%20%2849%29.png)

In the above example, we had several possible cases to consider. However, in many situations, there are only two main cases. Take for example, the following sentence: "If a number is divisible by 2, it is even. Otherwise it is odd." For these situations we have the ![](../.gitbook/assets/image%20%28143%29.png) block. It works like this:

![](../.gitbook/assets/image%20%28298%29.png)

Here, we didn't need to have an additional "if," because all whole numbers are either even or odd. If the boolean expression \(`x mod 2 = 0`\) evaluates to `false`, we know that the number is not even and thus must be odd.

#### mod Block

If you haven't seen the ![](../.gitbook/assets/image%20%28206%29.png) block before, it reports the remainder \(or "modulus"\) when the first input is divided by the second. For example, `5 mod 2` reports `1` because `5 / 2 = 2 remainder 1`. This block is especially useful for checking whether a number is divisible by another, because the remainder will be 0. ![](../.gitbook/assets/image%20%2893%29.png) is the same as asking if `x` is divisible by 2 \(i.e. that `x` is even\).

## Nested Conditions

A **nested conditional statement** is an `if` or `if else` statement inside the `else` part of another `if else` statement. If the predicate of the outer `if else` statement is false, then inner \(nested\) conditional statement will test its predicate and decide what to do.

Describe what this code segment will do.

![](../.gitbook/assets/image%20%28293%29.png)

## Predict the Output

Below are several blocks that use `if` and `if-else`. Predict what each one will do. Once you've done so, try running each of the blocks, which can be found [here](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/conditionals/predict-if-functions.xml).

#### abs block

You'll notice that a couple of the scripts below use the ![](../.gitbook/assets/image%20%28291%29.png) block. This block actually allows you to use many different mathematical functions. It shows up in the palette as ![](../.gitbook/assets/image%20%28285%29.png) . Just click the drop-down menu to select which function to use. "abs" is short for "absolute value." In case you're not already familiar, the absolute value of a number is just that number turned positive. For example, `abs(10)` is just `10`, while `abs(-2.5)` is `2.5`.

![](../.gitbook/assets/image%20%28231%29.png)

![](../.gitbook/assets/image%20%2813%29.png)

![](../.gitbook/assets/image%20%2848%29.png)

![](../.gitbook/assets/image%20%2842%29.png)

## Create If If-Else Blocks

Let's try making a few blocks that use if and if-else.

* Make a ![](../.gitbook/assets/image%20%28215%29.png) block that when given a light color, makes the sprite say the appropriate action. For example ![](../.gitbook/assets/image%20%28243%29.png) should say "go!"
* Make a ![](../.gitbook/assets/image%20%28229%29.png) block that takes in a percentage and makes the sprite say the associated letter grade. For example, ![](../.gitbook/assets/image%20%28259%29.png) should say "C."
* Make a ![](../.gitbook/assets/image%20%2824%29.png) block that takes in a temperature and says whether water will be liquid, solid, or gas.

