# Predicates

## Booleans

In order to represent the yes/no nature of condition phrases, we need a special type of value called a Boolean \(named after the great logician [George Boole](http://en.wikipedia.org/wiki/George_Boole)\). There are only two possible boolean values: `true` and `false` \(which correspond to "yes" and "no"\). These are represented in Snap_!_ by the blocks ![true](https://beautyjoy.github.io/bjc-r/img/blocks/true.png) and ![false](https://beautyjoy.github.io/bjc-r/img/blocks/false.png). 

## Predicates - Boolean Expressions

Blocks that report `true` or `false` are called **predicates**. 

![5 &amp;gt; 3 returns &apos;true&apos;](https://beautyjoy.github.io/bjc-r/img/cond/predicate-returning-boolean.gif)

These functions represent the yes/no questions. Predicate functions in Snap_!_ will always have the pointed, hexagonal shape \(like this: ![a predicate block](https://beautyjoy.github.io/bjc-r/img/cond/demo-predicate-block.png)\).

## Simple Predicates - Comparison Operators

Take a look at a few simple predicates that are built in to Snap_!_ Most of these can be found on the green "operators" tab. Examples include "&lt;", "&gt;", and "=".

## Complex Predicates - Logical Operators

Simple predicates have a single built-in block \(like ![=](https://beautyjoy.github.io/bjc-r/img/blocks/equals.png)\). Let's take a look at a few more complex examples:

* "If I am hungry and with my friends, I will order pizza." 
* "If I see George and Lisa at the mall, I will say "hello" to them."
* "If we are out of milk or eggs, go to the store."
* "If you are not enjoying the party, go home."

This brings us to three special predicates: `and`, `or`, and `not`.

![and](https://beautyjoy.github.io/bjc-r/img/blocks/and.png)

![or](https://beautyjoy.github.io/bjc-r/img/blocks/or.png)

![not](https://beautyjoy.github.io/bjc-r/img/blocks/not.png)

`And`, `or`, and `not` are all predicates that take in other predicates. These three predicates behave in ways you might expect from their meanings in English. 

When will the phrase "I am hungry and with my friends" evaluate to true? Only when both "I am hungry" and "I am with my friends" are true. If I wasn't with my friends, the entire phrase would certainly be false. 

We often summarize the behavior of predicates like `and`, `or`, and `not` using what are called truth tables. 

Here is the truth table for **`and`**:

| A | B | A and B |
| :--- | :--- | :--- |
| F | F | F |
| F | T | F |
| T | F | F |
| T | T | T |

Here, A and B are the two inputs to the `and` block. The `and` block only accepts boolean values, so A and B are either `true` \(T\) or `false` \(F\). 

Reading across each row tells us what `A and B` will output, given particular values of A and B. 

Here are the truth tables for **`or`** and **`not`**:

| A | B | A or B |
| :--- | :--- | :--- |
| F | F | F |
| F | T | T |
| T | F | T |
| T | T | T |

| A | not A |
| :--- | :--- |
| F | T |
| T | F |

Do these definitions fit with what you'd expect from English? Something you should notice is that "A or B" is still true even if both A and B are true. You might be tempted to argue that "or" should be false in this case \(consider the sentence "you may have hash browns or toast with your breakfast;" having both is generally assumed not to be an option\). 

However, when "or" is used in a predicate, we assume that it is "inclusive"  Think about the third example from earlier:

* If we are out of milk or eggs, go to the store."

 If we were out of both eggs and milk, we'd almost certainly still want to go to the store\). 

{% hint style="info" %}
The exclusive version of "or," often called ["xor,"](http://en.wikipedia.org/wiki/Xor) is available in many other programming languages, but it isn't included in Snap_!_
{% endhint %}

## Predicates Experiment

Read this script carefully, and make sure you understand why it produces this picture on the stage:

  
![clear
pen up
forever {
    go to \(random position\)
    if \(x position &amp;lt; y position\) {
        set pen color to purple
    } else {
        set pen color to orange
    }
    make a point
}](https://bjc.edc.org/bjc-r/img/2-complexity/dotscript.png) ![ Imagine a 45-degree line sloping upward toward the right, through the center of the stage. The area up and to the left of this line is purple; the area below and to the right is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/y-gtr-x.png)

Changing the predicate in the `if` block changes the picture. Discuss why the predicate![\(x position &amp;gt; 0\) and \(distance to apple &amp;gt; 100\)](https://bjc.edc.org/bjc-r/img/2-complexity/apple-script.png) generates this picture:

  
![There&apos;s an apple in the center. The entire left half of the stage is orange; so is a circle around the apple. What&apos;s left is purple.](https://bjc.edc.org/bjc-r/img/2-complexity/apple.png)

Match the predicate with the pictures. There are more expressions than pictures.

![](../.gitbook/assets/image%20%2810%29.png)

### Check for Understanding - Booleans

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/conditionals/booleans.html?topic=berkeley\_bjc%2Fintro\_pair%2F3-conditionals.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

