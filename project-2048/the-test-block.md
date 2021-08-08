# The Test Block

We've provided a large number of blocks that you can use in 2048. A big part of this project is understanding how to use these blocks, without needing to know how they work \(feel free to look at the code, but you shouldn't need to\). Your main task will be filling in all of the grey blocks listed in the spec; however, using the blocks that we have provided to you will make writing the required grey blocks much easier. In addition, in this assignment we're going to use a new HOF called test to verify the correctness of the gray blocks that we build.

To understand how the testing block works, let's start by looking at its structure.

![](../.gitbook/assets/image%20%28205%29.png)

Based on the structure of the block, we notice that the domain consists of a reporter \(inside the gray border, or ring\), a list, and two or more slots to pass in anything. This is very similar to the other HOFs we have already seen! The provided reporter will be the block we wish to test, the first set of slots will be for the input\(s\) to the function, and the final slot will hold the expected output of the provided reporter. Let's take a look at some examples.

![list of nouns, verbs, etc.](../.gitbook/assets/image%20%2856%29.png)

The above test is verifying that the subtraction block works properly. We leave the inputs of the subtraction block empty so that the provided inputs are fed into their spaces when we execute our test \(exactly like Combine!\), and then the provided output is checked against the actual output of the addition block. To add two inputs to the "input" section of the test block, you can hit the black arrow next to the input slot, just like you would do for a list! The output of the test block is a Boolean.

**For You To Do:**

Click on the "Proj3 Lab" sprite in the 2048 starter file \(the starter file is in the spec\), and you'll see two example tests for the addition operation. The first block tests that 1 + 1 = 2. Try running it, and you should get back `true` , since this test is correct. The second block performs 2 + 4 = 5. Try running it, and you should get that this test fails.

In this specific case, the problem is not the addition operation, but the input/output relationships that were wrong. In other words, we wrote an intentionally buggy test so you could see what happens when there is an input/output mismatch.

