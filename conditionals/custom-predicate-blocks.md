# Custom Predicate Blocks

{% hint style="info" %}
Predicate blocks return a true or false value
{% endhint %}

## Custom Predicate  &gt;=

We want to make our own _predicate_, a kind of block that reports either `true` or `false`. We have a "greater than" operator \(`>`\), an "equal" operator \(`=`\), and a "less than" operator \(`<`\), but we want a new "greater than or equal to" \(`>=`\) operator.

![](../.gitbook/assets/image%20%28142%29.png) ![](../.gitbook/assets/image%20%28288%29.png) ![](../.gitbook/assets/image%20%28148%29.png) 

This isn't really a hard problem, but we've learned from experience that many students have a hard time with it at first. So here are some suggestions if you get stuck.

Make sure that you choose the hexagonal `predicate` block shape in the initial `Make a block` dialog.

This is an _infix_ operator, i.e., the `>=` block name goes between the two input slots. So you'll have to use the left plus sign in the Block Editor.

You'll probably find the Boolean operators helpful, although they're not entirely necessary:

![](../.gitbook/assets/image%20%2881%29.png)

There are several correct ways to do this! It's okay if your answer is different from another group's answer, as long as it gives the right `true` and `false` answers.

If you _do_ have trouble with this problem, don't feel bad, but try to understand what's getting in the way, and when you see a solution, learn from it!

## Solutions

Here are four solutions to the &gt;= problem, in no particular order:

![if &amp;lt; else if = else](https://beautyjoy.github.io/bjc-r/img/prog/ge-ifelseelse.png)

![if &amp;gt; else =](https://beautyjoy.github.io/bjc-r/img/prog/ge-ifelse.png)

![not &amp;lt;](https://beautyjoy.github.io/bjc-r/img/prog/ge-notless.png)

![ &amp;gt; or =](https://beautyjoy.github.io/bjc-r/img/prog/ge-or.png)

I think this last one is the clearest, because it says in Snap_!_ the same thing you'd say in English: "A is greater than or equal to B if A is greater than B or A is equal to B."

## Custom Predicate - between 

Create a new predicate block that determines if a number is between two other numbers. The block should return `true` if the first number is between the two numbers or if it is equal to either of the numbers.

![](../.gitbook/assets/image%20%28144%29.png)

## Custom Predicates with Complex Booleans

Now we're going to write some blocks that utilize predicates like `and`, `or`, and `not`.

Write a ![](../.gitbook/assets/image%20%28229%29.png) block that reports whether a given day is a weekend. Let's assume that only Saturday and Sunday are part of the weekend.

Write a ![](../.gitbook/assets/image%20%28138%29.png) block. You could write this with or without your ![](../.gitbook/assets/image%20%28229%29.png) block, but it'll be much easier if you do.

Here is a block definition. Give it a more descriptive name, then re-write using no `if` blocks.

![](../.gitbook/assets/image%20%28289%29.png)

