# Custom Reporter Blocks

### Restricting Input Types <a id="input-types"></a>

Return to your max reporter block you created earlier.

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

