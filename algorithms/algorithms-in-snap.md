# Algorithms in Snap!

 Using [the framework provided](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/cur/programming/algorithms/../../../prog/algorithms/algorithms-framework-new.xml), implement a Snap_!_ block in the **Unsorted** sprite that finds a number in a list of unsorted numbers using the strategy that we discussed. The block should accept the target number \(the "needle"\) and a full list of numbers \(the "haystack"\) as arguments, and return the index of the number's position in the list. What was the strategy we discussed for unsorted lists, and how could you implement it? Two empty blocks are provided for you, one for unsorted and the other for sorted lists. Fill in the implementation for each block. Using the framework, determine how their running time changes as the list size increases. Which is faster for a list of size 5? 50? 500? 5000? Why do you think this is?

### Searching Unsorted Data

![](../.gitbook/assets/image%20%28260%29.png)

Unsorted data doesn't give you a lot to work with. Your knowledge is limited to strictly the most obvious information: the numbers themselves. This makes strategy somewhat non-existent; the best you can do, on average, is to simply start at the beginning and search through the list one by one. This approach can become incredibly slow if we're dealing with a lot of data, but is actually fairly quick when working with smaller amounts of data. In addition, the block is relatively straightforward to create and doesn't require the data to be put into a particular order to work. The block should return the location of the number in the list, or -1 if the number doesn't exist in the list.

### Searching Sorted Data

![](../.gitbook/assets/image%20%28106%29.png)

You could say that putting information in a particular order \(lowest to highest, for example\) actually creates new information. Instead of being a simple list of numbers, sorting the information adds order and allows us to make additional assumptions that we weren't able to make before. This type of information is different from the numbers themselves: it is not stored in a variable or list, but becomes a property of the information itself. We can use the property to reduce the number of checks we have to do to find a particular number. However, the list must be sorted before we can make use of the order.

Searching through sorted data, while faster, also requires a more complicated block. We won't need to search through every space in the list anymore -- we can assume that many of them won't work. We can keep track of the range of numbers in a list that are a possible solution to the problem \(see diagram\) by recording the minimum and maximum slots that could possibly contain our number. This range should shrink after each guess because you can throw away the half of the numbers on the wrong side of the center point. Here's how things should generally work:

![](../.gitbook/assets/image%20%28151%29.png)

1. The range of possibilities starts off including every number in the list \(the minimum is position \#1 and the maximum is the final position\). Let's say that we're searching for the number 33 as shown in the diagram. Start your search around the middle of the list. Check the value of the number there.
2. If the number at the spot you searched is greater than 33, set the maximum to the slot before the one you just searched \(after all, 33 CAN'T be on the larger side if it's is smaller than the one you just checked!\). If the number is smaller than 33, set the minimum to the slot after the one you searched.
3. Check the middle position of your new range. Repeat step 2 for this new range and reduce the range further.
4. Continue to repeat steps 2 & 3 until either \(a\) you find the number you're looking for or \(b\) you get in a position where the minimum is greater than the maximum \(try to work out an example where this happens\). If \(b\) happens, it means that the number doesn't exist in the list. In this case report -1. 

### Flying Even Higher - Improving our Number Finder

Let’s say this application is going to be used to find many numbers every time it is launched -- possibly the same number multiple times. How could we speed this process up even more?  
  
If the user may be searching for the same number multiple times, it seems ridiculous to calculate the answer each time that they ask. Why don’t we remember the answer after it’s been calculated instead? Remembering previously calculated information is called memoization \(not memorization\) in computer science. It is a powerful technique that can be used to speed up programs that have redundant calculations.  
  
Let’s implement a third block in our project that uses memoization to remember the location of numbers that have already been found. This block will be very similar to our the second block you built, the sorted number finder.

![](../.gitbook/assets/image%20%28119%29.png)

We’ll use a list to keep track of the locations of numbers that we’ve found already: the index of each element in the list will be the number we’re looking for and the corresponding value will be the location where that number was found. If the value at a particular index is 0, that means that we haven’t looked for the number yet and if the value is -1 then that means that the number doesn't exist in the list. Here is an algorithm describing how the new block should progress using the new memoization list:

1. Start off setting all of the slots in _memory_ to 0 because we haven't found any numbers yet. \(already completed for you\)
2. Check the list _memory_ to determine if the number in question has already been found.
3. If so, report the saved location. If not, we’ll have to calculate it.
4. Find the number’s location using the sorted technique we’ve used in the past.
5. Save the location of the number in the _memory_ list so that we don't have to go through this pain again.

  
Each value will now be computed a maximum of one time. Now that’s fast, but Test for yourself how much faster this method is by clicking the timer script.  
  
Consider the following questions:

* When is memoization most useful?
* What are some trade-offs of using memorization?

### Too Many Blocks

There’s only one problem with our search project: we’ve got three different blocks that all do the same thing \(finding a number in a list\). That’s way more complicated than it needs to be...how could we use abstraction to make this clearer and simpler for others who want to find numbers in a list?

Here’s a thought: what if we created a single block "find number x in list y" that made no mention of how it found the number. The user of the block could assume that it would do what it said without worrying about the technicalities of how it gets it done. Then, even if you started with a terribly slow version of the block, you could easily update the algorithm it used without changing anything outside of the block itself. The input and output would remain the same -- only the steps to get from one to the other would change.

This is the beauty of abstraction with algorithms: users are able to assume that a particular block works without having to understand all of the details of the algorithm itself! Did you investigate the sort block included with this lab? You didn’t have to -- you could just assume that it worked!

In fact, each of the blocks in Snap_!_ has an algorithm that tells it how to do what it does. Think how much harder it would be to work with Snap_!_ if you had to understand how each block worked before you could use it!

