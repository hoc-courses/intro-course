# Custom Reporter Blocks

## Create a Custom Reporter - max

Let's try writing our own reporter block!  We will make a block called `max` that takes two numbers as input and reports the bigger value \(the maximum\).

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-16.png)

* Click `Make a block` and select the `Operators` tab. We want a reporter block. This will give the block its round shape as shown above. As the name implies, reporter blocks can report a value. In the image below, you can see that we used the % shortcut for making input variables.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-17.png)

* This should give you a blank Block editor. We need to figure out what should be reported. To keep track of the value to be reported, we are going to make another variable. 
* There are two ways to do this: Use a `Script Variable` block. You can click on the name of the variable and change it to bigger value. Alternatively, you can just report which of the two is larger.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-18.png)

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-19.png)

### Input Types <a id="input-types"></a>

We want the `max` block to work only for numbers. Yet, you can type text in!

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-20.png)

We are going to limit the `max` block to accept only numbers as arguments.

* Open the Block Editor for the `max` block and click on the input `x`

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-21.png)

* Then, click on the right arrow in the pop-up box shown above. This will open the dialog box shown below. This allows us to specify the shape of the slot. We want a numbers-only slot \(as shown selected below\). We can also specify that we want the variable to have a _default_ value; this is similar to blocks like move that always start out with the default value 10.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-22.png)

* Modify both the `x` and `y` variables to take only numbers and to have the default values of `5` and `10`, respectively. Your `Block Editor` should then look like this, with the default values shown in the header.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-23.png)

* When you click OK, you should be able to see your block in the Operators tab, with the default values filled in. Also, note that you will no longer be able to enter text.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-24.png)

## More Custom Blocks

### Composition

Your challenge is to make the following blocks work by composing several functions together \(and then maybe a little extra work\):

1. A three-input addition operator that accepts only numbers.![Three-argument addition operator](https://beautyjoy.github.io/bjc-r/img/prog/3-arg-addition-block-BYOB.gif)
2. A reporter block named "sum of two smallest" that takes three numbers as inputs, and reports the sum of the two smallest \(the example shown below would report 9\):![sum of two smallest block](https://beautyjoy.github.io/bjc-r/img/cond/sum-of-two-smallest.png)
3. A predicate block named "Are any equal?" that compares 3 numbers and returns true if any two are equal to each other \(the example shown below would return true\):![Are any equal? predicate block](https://beautyjoy.github.io/bjc-r/img/building-blocks/composition-are-any-equal.png)

### Loop

Now let's consider a slightly more complicated block that makes use of a loop. It accepts two numbers as inputs \(`start` and `end`\) and finds the sum of all of the numbers in the range from `start` to `end`, inclusive.![sum of nums in a range](https://beautyjoy.github.io/bjc-r/img/blocks/sum-of-numbers-between-8-and-10.gif)

When `start = 8` and `end = 10`, the value reported by this function should be `27` \(8+9+10\). However, the attempts at a solution shown below have some bugs. See if you can fix the bugs in the code below so that each version reports the correct sum:

_Note:_ click on any of the pictures to go to a Snap_!_ file containing the code.[![buggy sum of nums set block](https://beautyjoy.github.io/bjc-r/img/debugging/set-bug-sum-of-range.png)![buggy sum of nums no report](https://beautyjoy.github.io/bjc-r/img/debugging/buggy-sum-of-nums-no-report.png)![buggy sum of nums repeat until](https://beautyjoy.github.io/bjc-r/img/debugging/buggy-sum-of-nums-repeat-until.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/debugging/sum-of-nums-buggy.xml)

