# Conditionals & Reporters

So far, you've practiced writing scripts that carry out short sequences of commands. One thing that all of these scripts have in common is that they run every single one of their blocks, no matter what. But what if we wanted to program a more complex application? Will we always want to run all of our code every time we run the program? Let's think about an example:

* Write a simple banking program that allows a user to withdraw from and deposit money into an account and to check their balance. At the start of the program, we will prompt the user to input what they'd like to do. If they choose to deposit or withdraw, we'll need to ask them how much, and then increase or decrease their balance accordingly. On the other hand, if they ask for their balance, we simply need to display it.

How might you write this program. In particular, think about the individual pieces you would need to create the bigger program.

Now that you've thought about the above examples, let's go over the pieces you'd need for one of them. In the banking example, you'll need to write code to ask for the user's input, withdraw money from an account, deposit money into an account, and to display the balance to the user. Returning to the question we mentioned earlier, will we always want to run all of these pieces every time we run the program? The answer should be "no." 

For example, if the user chooses to display their balance, we certainly don't want to run the code that withdraws money from their account. This idea can be represented in the form of conditional, or "if-then," statements. The banking example can be expressed as follows:

* Ask the user what they'd like to do.
* **If** the user selects "withdraw," **then** ask them how much to withdraw and subtract that amount from their account.
* **If** the user selects "deposit," **then** ask them how much to deposit and add that amount to their account.
* **If** the user selects "display balance," **then** look up their balance and display it.

Notice how the three latter bullets all follow the same format: "if **A**, then **B**," where **A** and **B** are both phrases. Do you notice anything special about the **A** phrases and the **B** phrases in the above examples? All of the **A** phrases \(between "if" and "then"\) can be thought of like yes/no questions. For example, "If the user selects 'withdraw'" can be re-phrased as "Did the user select 'withdraw?'," to which the answer should always be "yes" or "no." On the other hand, the **B** phrases \(after "then"\) all are more like series of commands, telling the program what to do.

Fortunately, the Snap_!_ blocks that represent "if-then" statements are very similar to English. Below is an example of what the banking program might look like. Try reading the program aloud. It should sound like pretty reasonable English! However, if you don't understand parts of it, don't worry. We'll get there soon!

![](../.gitbook/assets/image%20%2871%29.png)

