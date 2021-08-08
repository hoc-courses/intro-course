# Linear Time

You may have noticed that if you increased `max` by a factor of two, then the computer took approximately twice as much time to fill the `numbers` list.  Similarly, if you increased `max` by a factor of ten, then the computer took approximately ten times as much time; if you increased `max` by a factor of 100, then the computer ran approximately 100 times longer.  In general, as we scale the size of the input by a certain amount, we also scale the running time by the same amount.  We call these algorithms **linear-time** algorithms, because if we were to plot the runtime of one such algorithm against the size of its input, we would get a line.

    Why is the algorithm a linear-time algorithm?  When `max` was set to `20`, we had to add 20 numbers to the `numbers` list; when `max` was set to `40`, we had to add 40 numbers to the number list.  In other words, as we scaled `max`, we also scaled how many numbers we had to add to the `numbers` list by the same amount.  Linear-time algorithms are also much sought-after in computer science, and for many problems, they are the fastest algorithms you can find.

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/algorithms/timing/quiz-searching-through-time.html?topic=berkeley\_bjc%2Fareas%2Falgorithm-complexity.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}



