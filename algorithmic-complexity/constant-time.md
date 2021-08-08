# Constant Time

 In the timing experiments of the previous section, you may have noticed that the computer takes approximately the same time to increment a number, even though the number was made progressively larger.  Computer scientists \(programmers and theorists\) thus call incrementing a number a **constant-time** operation.  In fact, _any_ basic arithmetic operation \(addition, subtraction, multiplication, division, and exponentiation\) is considered to be a constant-time operation.

 Notice that we call these operations _constant-time_ operations, but we don't actually say how much time they take.  Different computers will take different amounts of time to perform the same operation.  To report the exact time of any algorithm, we would have to also report the physical configurations of the computer that the algorithm was run on.  This gets very difficult and annoying very fast, especially with the almost infinite variety of computers available today.  Instead, we focus on how the running time of an algorithm scales as we scale its inputs to larger and larger sizes, because this is a property of the algorithm itself, and is independent of the computer that it is run on.

 Why did the computer take approximately the same amount of time to increment a number, even though that number was getting larger?  Think about how you would add one to a number, back from your elementary school days; this is similar to how a computer does its arithmetic \(ignoring technical details\).  The elementary school way of adding numbers goes digit by digit, and so the amount of time it takes for you to add two numbers depends on how many digits each number has.  As we doubled the number we were incrementing, we didn't consistently add digits to it, and so the computer took approximately the same time.  Even as we began scaling the number by ten, the computer \(and you!\) takes a relatively small amount of time to account for the extra digit, so the total time remains approximately constant.

 Constant-time operations are the Holy Grail of computer science algorithms, and unfortunately, most algorithms are _not_ constant-time, as we will soon see.



For this section, we will be using [this timing framework](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/cur/programming/algorithms/timing/../../../../prog/algorithms/timing-framework.xml).  It is very similar to the framework you constructed earlier, but it also has the stubs for a few blocks that we will be filling in.  The first block that we will fill in is already on stage:

![](../.gitbook/assets/image%20%28105%29.png)

    This block should fill the input list with all of the numbers from `start` to `end`.  If working correctly, the version used on stage should generate all of the numbers from `1` to `max`, where `max` is a number that we will change when running timing experiments, and should add them to the `numbers` list.

    First, talk to your partner and discuss an algorithm that you can use to fill the input list with all of the numbers from `start` to `end`.  Once you both have decided on an algorithm, complete the body of the block.  Now, run the script with `max` set to `10`.  Run it a few times to get an idea of the average time the computer takes to generate this list \(to the nearest tenth of a second\); you don't need to be exact!  Repeat the experiment with `max` set to `20`, `40`, `100`, `200`, and `1000`.  Do you see a pattern?

