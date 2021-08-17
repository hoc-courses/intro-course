# Composition

Suppose we want the squares of all the items of a list of numbers. That's a straightforward `map` problem:

![](../.gitbook/assets/image%20%28104%29.png)

 Now suppose instead that we want to select the odd numbers from a list of numbers. It's a little tricky figuring out how to tell if a number is odd, but apart from that it's a straightforward `keep` problem:

![](../.gitbook/assets/image%20%28231%29.png)

But what if we want the squares of the odd numbers? This is neither a simple `map` nor a simple `keep`, but combines aspects of both. And we can solve the problem by using the value reported by the `keep` as the list input to `map`:

![](../.gitbook/assets/image%20%28246%29.png)

  
Don't be confused about which inputs do and don't have rings. It's the square **function** and the are-you-odd? **function** that we use as the first input to each higher order function. But, even though `keep` itself is a function, it's the **list** reported by `keep` that we're using as the second input to `map`.

