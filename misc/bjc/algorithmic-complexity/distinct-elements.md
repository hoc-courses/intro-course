# Distinct Elements

Consider the following problem: I have a list of numbers and I want to know if the numbers in this list are _distinct_. In other words, I want to know if there are any repetitions in my list. This kind of question pops up frequently in computer science: for example, when returning search results, Google would like to ensure that all of the search results are different from each other \(as far as possible\). Here is a first attempt at an algorithm \(which is a series of steps\) to solve the problem:

  
**Step 1**. I take the first number of the list, and compare it with all of the other numbers in the list \(the second number, the third number, and so on\). If, at any point, I see the same number again, I stop and tell the user that the numbers are not distinct.  
  
**Step 2**. If I complete step 1 without stopping, I take the second number of the list, and compare it with all of the other numbers in the list \(the third number, the fourth number, and so on\). If, at any point, I see the same number again, I stop and tell the user that the numbers are not distinct.  
  
**Step 3**. I repeat the two steps above for all of the numbers in the list, each time taking a number from the list and comparing it with all of the following numbers.  
  
**Step 4.** If I am done with all of the numbers in the list, I stop and tell the user that the numbers _are_ distinct.

Take a moment to understand the algorithm, and ask any questions that you may have. Using the algorithm above, complete the body of the following block in the `Variables` menu:

![](../../../.gitbook/assets/image%20%2817%29.png)

Once we are done with the block, we need to figure out the **worst-case** running time of the algorithm: how long will this algorithm take on the worst possible input? By "worst", we mean an input that will cause the algorithm to work the most, or to run through the most steps. For this algorithm, for example, what is the worst possible input?

Well, since the algorithm only ever stops partway if the numbers in the list are not distinct, we need a list whose numbers are distinct, so that the algorithm will have to look at all the numbers in the list. We already have one such list: the list of numbers from `1` to `max`! \(This is turning out to be quite a useful list.\) Let's use it!

Replace the "Gauss" block from the previous section with the `are the numbers of list distinct?` block that you just made. The list that we are going to test is the `numbers` list, as we explained above. \(Also, modify what Alonzo says at the very end of the script to subtract the extra second that he uses to tell us whether the numbers in the list are distinct.\)

Run the timing script with `max` set to `10`. Again, run the script a few times to get an idea of the average time the computer takes to determine if the numbers in the `numbers` list is distinct.

Repeat the experiment with `max` set to `20`, `40`, and `100`. What happens to the running time of the block when the size of the list is doubled? What happens when the size of the list is scaled by a factor of 10? \(If you have quite a bit of time, you may want to try and see how long the algorithm takes with `max` set to `1000`.\)

