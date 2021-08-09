# Swapping List Values

 We want to make a block that swaps two items in a list. The block takes two numbers, representing positions of items in the list, and the list itself as its inputs; it swaps the positions of those items in the list. Make this block in the List category; it's a command block. Set the input types of `itemX` and `itemY` to number, and the type of `data` to list.

![](../.gitbook/assets/image%20%2826%29.png)

When you click `Apply`, you should be able to see the block with two round number input spots and one list input spot. ![](../.gitbook/assets/image%20%2851%29.png) 

\(By the way, we called the list input `data` instead of `list` because people have commented that it's too easy to confuse a `list` variable block with the block to create an empty list: ![orange list variable](https://beautyjoy.github.io/bjc-r/img/list/orangelist.png)![red list constructor](https://beautyjoy.github.io/bjc-r/img/list/redlist.png) .\)  


Finish entering the complete script:

![](../.gitbook/assets/image%20%2812%29.png)

Here is an example of how the block will be used: If we run the block with the arguments

![](../.gitbook/assets/image%20%28227%29.png)

where `game board` is the list

![](../.gitbook/assets/image%20%28190%29.png)

then the list should become

![](../.gitbook/assets/image%20%28210%29.png)

The `replace item` blocks in this script are an example of a new technique, list _mutation_--changing items in an existing list, instead of creating a new list the way `map` and `keep` do. As in this example, mutation can be more efficient than recopying the entire list except for the two changed items. On the other hand, mutation introduces the possibility of new kinds of bugs that can't happen with _functional_ programming, the technique we've been using with lists until now. If two parts of a large program are using the same list for different purposes, and one part mutates the list, the other part will get confused. That's why we showed you functional programming first, and why functional programming should be your first instinct.

We _have_ used mutation before with non-list data; for example, the `for` block changes the value of its variable `i` each time through the loop. Mutation isn't so dangerous in that context, because that variable exists only inside the `for` loop, there's no way another part of the program can be relying on an old value. Mutating _global_ variables does have the same risk, though, which is why we've been saying that script variables are a better choice when possible. But a game board is an example of a value that's unavoidably both global and mutable. We'll go into this further in the next lesson.

