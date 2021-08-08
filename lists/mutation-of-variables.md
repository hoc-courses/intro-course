# Mutation of Variables

Suppose I have a global variable named `foo` , and I define the following two blocks:

![](../.gitbook/assets/image%20%2883%29.png)

![](../.gitbook/assets/image%20%2866%29.png)

Now I run the following script:

![](../.gitbook/assets/image%20%282%29.png)

Will the final value of foo be 100? 105? 120? or 125? Try it and see.

Now do the following similar experiment, but with a list as the value of `foo` :

![](../.gitbook/assets/image%20%2855%29.png)

![](../.gitbook/assets/image%20%28106%29.png)

![](../.gitbook/assets/image%20%2881%29.png)

What items will be in `foo` after running this script?

Why do these two experiments give different results?

It's not surprising that the two blocks that specifically change the global variable `foo` succeed. But how come you can add a new item to a list passed into a block as input, whereas you can't change a numeric variable passed in as input?

Snap_!_ is actually behaving consistently in these two cases. To understand why, you have to keep clear in your mind the difference between a _value_–a number, text string, Boolean \(true/false\), or list–and a _variable,_ which is essentially a connection between a name and a value. \(This is not precisely the definition of "variable" you'd learn in a programming language design course, but it's close enough until you have to implement a programming language yourself.\)

As in most programming languages, the inputs you provide to a block in a Snap_!_ program are _values._ The block doesn't know how the value was provided: typed directly into an input slot, computed by a reporter dragged into the slot, or taken from a variable dragged into the slot.

If that went over your head because it's too abstract, consider this script:

![](../.gitbook/assets/image%20%28155%29.png)

You wouldn't expect _that_ to change the value of `foo` to— To what? 123? 117? It just doesn't make sense to expect this to change `foo` at all. The input to the `add 20 to` block is the number 103–the _value_ of ![foo+3](https://beautyjoy.github.io/bjc-r/img/list/foo+3.png)–not the variable. The same is true in the original experiment; the input to `add 20 to` is the number 105 \(because the `add 5 to foo` block specifically changed `foo` \), not the variable `foo` itself.

The `change` block in the definition of `add 20 to` does change a variable: the variable it says it changes, namely `var` . That variable is local to the block's defining script, so changing it doesn't affect the rest of the program at all. Local variables are temporary; when the block finishes, the variable is gone.

What if the value of `foo` is a list? Unlike numbers, lists themselves are mutable. \(_Variables_ are mutable, too, which is why we're having this discussion, but only when the variable name itself appears in a `set` or `change` block.\) After the two `append` blocks in the second experiment are run, the value associated with variable `foo` is _the same list_ as it was before. But that list now has more elements. We say that it "maintains its identity" even though its contents have changed.

