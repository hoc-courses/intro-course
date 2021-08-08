# Complex Predicates - Comparison Operators

Simple predicates have a single built-in block \(like ![](../.gitbook/assets/image%20%2895%29.png) \). Let's take a look at a few more complex examples:

* "If I am hungry and with my friends, I will order pizza." 
* "If I see George and Lisa at the mall, I will say "hello" to them."
* "If we are out of milk or eggs, go to the store."
* "If you are not enjoying the party, go home."

 In past examples, we've seen conditionals that contain a single predicate \(![=](https://beautyjoy.github.io/bjc-r/img/blocks/equals.png), ![&amp;lt;](https://beautyjoy.github.io/bjc-r/img/blocks/less-than.png), etc.\). We could write a single block for each of the above conditionals, but that might be a bit weird. In the first sentence, for example, this would entail writing an "am hungry and with friends?" predicate. This seems a little strange because the "am hungry" and the "with my friends" parts aren't necessarily related; it doesn't make sense to put them as a single predicate. So, instead, we might write separate "am hungry?" and "with friends?" predicates and combine them in some way. 

This brings us to three special predicates: `and`, `or`, and `not`.

![](../.gitbook/assets/image%20%2853%29.png)

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

