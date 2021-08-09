# Composition - Part 1

Suppose we want the squares of all the items of a list of numbers. That's a straightforward `map` problem:

![](../.gitbook/assets/image%20%28104%29.png)

 Now suppose instead that we want to select the odd numbers from a list of numbers. It's a little tricky figuring out how to tell if a number is odd, but apart from that it's a straightforward `keep` problem:

![](../.gitbook/assets/image%20%28229%29.png)

But what if we want the squares of the odd numbers? This is neither a simple `map` nor a simple `keep`, but combines aspects of both. And we can solve the problem by using the value reported by the `keep` as the list input to `map`:

![](../.gitbook/assets/image%20%28244%29.png)

  
Don't be confused about which inputs do and don't have rings. It's the square **function** and the are-you-odd? **function** that we use as the first input to each higher order function. But, even though `keep` itself is a function, it's the **list** reported by `keep` that we're using as the second input to `map`.

  
We're building up to one the great beautiful procedures you'll see in this course: We want to take a phrase, such as "Beauty and Joy of Computing," and report its acronym, the word BJC. 

You've explored two of the pieces of this problem in previous activities:

* Select only the words with five or more letters.
* Make a list of the first letters of the words.

Review those activities if you don't remember how to solve those problems.

But there are two more steps, one at the beginning of the problem and one at the end, both related to the fact that people \(the users of your program\) want to see words and phrases in the form of text strings, but as you've seen, it's much easier to compute functions of those words and sentences if we have them in the form of lists, so we can use the higher order functions you're learning. 

To translate from a text string to a list of words, you will need to import the `sentence->list` block by importing the _Words and Sentences_ library. To import the library, click on the file icon in the upper left hand corner of Snap_!_, select _Libraries_, and import the _Words and Sentences_ library.

![](../.gitbook/assets/image%20%28185%29.png)

![](../.gitbook/assets/image%20%28211%29.png)

 As usual, you see only the first three list elements in the speech balloon, but you're told at the bottom that the length of the list is 5, as it should be for the five words in the given phrase.

Once we have the list, we can use the tools we've already built to get a list of the first letters of the long words. What we want, though, is a single word as the reported value. We can use one of the higher order functions to join the letters into a string.

**Try this:** Should we use `map`, `keep`, or `combine` for this purpose?

Here's the final result. Oops! The word "Joy" is shorter than five letters, but it's still an important word in the acronym. We need a better algorithm.

![](../.gitbook/assets/image%20%28288%29.png)

![](../.gitbook/assets/image%20%2858%29.png)

**Try this:**  
Modify the `acronym` block so that, instead of keeping long words, it keeps words that start with a capital letter. \(Hint: Experiment with the `unicode of` block.\)

![](../.gitbook/assets/image%20%28308%29.png)

![](../.gitbook/assets/image%20%28251%29.png)

![](../.gitbook/assets/image%20%28176%29.png)

