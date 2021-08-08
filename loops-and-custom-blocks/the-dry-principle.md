# The DRY Principle

Some of the principles we've learned so far can be summed up by a term that is used frequently in Computer Science: DRY.

**DRY** stands for **Don't Repeat Yourself,** a basic principle of software development aimed at **reducing repetition** of information.

> _Every piece of knowledge must have a single, unambiguous, authoritative representation within a system. - The Pragmatic Programmer_

#### Why is DRY important?

* Write code once, use it often.
* Change code in one place, see the change in all instances.
* Less code is good: It saves time and effort, is easy to maintain, and also reduces the chances of bugs.

#### Dry Violations

Writing/copying and pasting the same code or logic again and again.

Let's start out with a simple example. We want to draw a square. Here is an algorithm for drawing a square.

![](../.gitbook/assets/image%20%284%29.png)

Now let's draw a series of squares.

![](../.gitbook/assets/image%20%28286%29.png)

Obviously, this is violating the DRY principle. There are a few common programming techniques to allow you to adhere to the DRY principle.

### Refactoring

Refactoring is when you take some code that is functionally correct and modify it to do the same task more efficiently.

### Loops

In the code below, we refactored the code into fewer instructions by utilizing the repeat block to execute the same instructions three times.

![](../.gitbook/assets/image%20%28161%29.png)

### Nested Loops

We can further refactor our code by adding another loop nested within the outer repeat block to repeat the drawing of each side of the square.

![](../.gitbook/assets/image%20%2873%29.png)

### Procedures allow Abstraction

The main goal of abstraction is to handle complexity by hiding unnecessary details from the user. That enables the user to implement more complex logic on top of the provided abstraction without understanding or even thinking about all the hidden complexity.

We are going to apply that principle here to create a **command** block \(no return value\) that will be responsible for performing the instructions necessary to draw a square.

![](../.gitbook/assets/image%20%28226%29.png)

And now the code has been greatly simplified. We no longer need to think about the individual instructions necessary to draw a square. We can simply use the `drawSquare` command to perform the instructions whenever we need to draw a square.

### Procedures allow Re-use

Another important feature of writing procedures is that they can receive input that allows them to work in a wider range of circumstances.

In our `drawSquare` command, it currently hard-codes the size of the square. While this works for this particular use-case, it would be more re-usable if it allowed the user to specify the size of the square. This is done by adding input variables to a procedure.

![](../.gitbook/assets/image%20%28290%29.png)

### A DRY Solution

And now we have our finished DRY algorithm to draw a series of three squares.

![](../.gitbook/assets/image%20%28125%29.png)

## Try it

Below is some code to draw a tic-tac-toe board. Your goal is to create blocks that make this code simpler.

![Tic-Tac-Toe Board Drawer](https://beautyjoy.github.io/bjc-r/img/abstraction/complicated-tic-tac-toe.png)

Some things to remember:

* As a first step, break up this drawing task into meaningful sub-tasks. We suggest doing this working with pen and paper, not while looking at the code!
* Give your new blocks appropriate names. You want to make it easy to read the code—at its best, like natural, English sentences— and understand what it does.

Use this [Snap_!_ project](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/building-blocks/complicated-tic-tac-toe.xml), duplicate of the image above, to get started.

