# Complex Predicates - Comparison Operators

Simple predicates have a single built-in block \(like ![](../.gitbook/assets/image%20%28124%29.png) \). Let's take a look at a few more complex examples:

* "If I am hungry and with my friends, I will order pizza." 
* "If I see George and Lisa at the mall, I will say "hello" to them."
* "If we are out of milk or eggs, go to the store."
* "If you are not enjoying the party, go home."

 In past examples, we've seen conditionals that contain a single predicate \(![=](https://beautyjoy.github.io/bjc-r/img/blocks/equals.png), ![&amp;lt;](https://beautyjoy.github.io/bjc-r/img/blocks/less-than.png), etc.\). We could write a single block for each of the above conditionals, but that might be a bit weird. In the first sentence, for example, this would entail writing an "am hungry and with friends?" predicate. This seems a little strange because the "am hungry" and the "with my friends" parts aren't necessarily related; it doesn't make sense to put them as a single predicate. So, instead, we might write separate "am hungry?" and "with friends?" predicates and combine them in some way. 

This brings us to three special predicates: `and`, `or`, and `not`.

![](../.gitbook/assets/image%20%2867%29.png)

`And`, `or`, and `not` are all predicates that take in other predicates. These three predicates behave in ways you might expect from their meanings in English. 

When will the phrase "I am hungry and with my friends" evaluate to true? Only when both "I am hungry" and "I am with my friends" are true. If I wasn't with my friends, the entire phrase would certainly be false. 

We often summarize the behavior of predicates like `and`, `or`, and `not` using what are called truth tables. 

Here is the truth table for **`and`**:

#### A AND B

![](../.gitbook/assets/image%20%28369%29.png)

Here, A and B are the two inputs to the `and` block. The `and` block only accepts boolean values, so A and B are either `true` \(T\) or `false` \(F\). 

Reading across each row tells us what `A and B` will output, given particular values of A and B. 

Here are the truth tables for **`or`** and **`not`**:

#### A OR B

![](../.gitbook/assets/image%20%28378%29.png)

#### NOT A

| A | not A |
| :--- | :--- |
| F | T |
| T | F |

![](../.gitbook/assets/image%20%28370%29.png)

