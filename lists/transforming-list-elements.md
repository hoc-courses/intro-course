# Transforming List Elements

In the last activity we made this list of nouns:

![](../.gitbook/assets/image%20%28191%29.png)

Now suppose we'd like to be able to vary our noun phrases by sometimes using one of these nouns in the plural. So we need a way to add the letter "s" to each item of the list. Find the **map** block near the bottom of the Variables palette and use it this way:

![](../.gitbook/assets/image%20%287%29.png)

The first input to the `map` block has a form you haven't seen before this:

![](../.gitbook/assets/image%20%28184%29.png)

The grey ring means that the input should be a function. What we mean by this is basically the same thing as the f\(x\)=3x+7 kind of function in algebra, except that it doesn't have to be a numeric function. In this case the function we want is "join the letter 's' after the given word." When you drag the `join` block into the `map` input slot, the grey ring is still visible, to remind you that the input is a function, not the word that you'd get from some particular `join`ing.

Instead of using a variable, like the x in f\(x\), to represent the input to the function, we leave one of `join`'s input slots as an empty box. This is supposed to remind you of the notation 3×☐+7 \("three times box plus seven"\) that you learned for functions in elementary school before you knew about variables.

  
**Try this:** Modify your `noun phrase` block so that half the time it uses a plural noun. Note that, if you use a plural noun, the article has to be "the," rather than "a."

  
Here are some more examples of using `map` to compute some function of every item of a list:

![](../.gitbook/assets/image%20%2830%29.png)

![](../.gitbook/assets/image%20%28266%29.png)

![](../.gitbook/assets/image%20%2850%29.png)

In that third example, there are two empty boxes in the function, so it's ☐×☐, which squares each number.

  
**Try this:**  
In the last activity we made a list of Beatles:

![](../.gitbook/assets/image%20%28211%29.png)

  
Use `map` and this list to get a list of just the first names of the Beatles.

![](../.gitbook/assets/image%20%2847%29.png)

  
A function that, like `map`, takes another function as an input is called a higher order function. In the next two activities you'll meet two more higher order functions.

