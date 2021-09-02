# Constant vs Linear Time

We will now see an example where the runtime of an algorithm really does make a difference. Remember the game you played with young Gauss at the beginning of lab? We will implement the game in Snap_!_ .

[Earlier in the lab](https://beautyjoy.github.io/bjc-r/cur/programming/loops/sum-things-up.html), you made a block that returned the sum of numbers between `1` and `max`. In the `Variables` menu, you will see two blocks:

![](../../../.gitbook/assets/image%20%28172%29.png)

The first block sums up the numbers in the `numbers` list the normal, "non-Gauss" way: walking through the list and adding the numbers one by one. The second block sums up the numbers the "Gauss" way: using the formula `(N + 1) * N/2`, where, in this case, `N` is the same as `max`. \([How did we get this formula?](https://beautyjoy.github.io/bjc-r/cur/programming/algorithms/competing-with-young-gauss.html)\) Complete the bodies of these blocks.

Once you are done, drag the first block \(the "non-Gauss" block\) onto the stage and place it immediately after the `add all numbers between 1 and max` block. Also, move the `reset timer` block _after_ the `add all numbers between 1 and max` block, since we only need to time how long the "non-Gauss" block takes to sum the numbers in the `numbers` list.

Now, run the script with `max` set to `10`. Again, run it a few times to get an idea of the average time the computer takes to sum the numbers up. Repeat the experiment with `max` set to `20`, `40`, `100`, and `1000`. Based on your observations, what kind of runtime does the "non-Gauss" block have: constant, linear, or neither? Why do you think this is the case?

Replace the "non-Gauss" block with the "Gauss" block. Once more, run the script with `max` set to `10`. Again, run it a few times to get an idea of the average time the computer takes to sum the numbers up. Repeat the experiment with `max` set to `20`, `40`, `100`, and `1000`. Based on your observations, what kind of runtime does the "Gauss" block have: constant, linear, or neither? Why do you think this is the case?

In the experiments in the previous section, we concluded that the "non-Gauss" block had a linear runtime, while the "Gauss" block had a constant runtime.

Both blocks were answering the same question: I have a list of numbers from `1` to `max`, and I want to know what the total of these numbers is.  The "non-Gauss" block is a great first attempt at solving the problem, and works rather fast even for large lists.  However, its main disadvantage is that its runtime is nonetheless dependent on the length of the input, and so the longer the list, the longer you will have to wait to get an answer.  The "Gauss" block, however, does not have to go through the numbers in the list; all it ever needs, every time, is one piece of information: the length of the list, which \(in this case\) is also the value of `max`.  Once you give it this information, it will always perform the same number of arithmetic operations, regardless of whether the list is 10 elements long or 10 million, and that instantly makes it the better algorithm.

Many computer scientists work every day to try and get this kind of an improvement in running time, or to try and show that you can't get any faster.

