# Timers

We have seen how Snap_!_ can be used to wait for a certain time before reporting anything. Snap_!_ also allows us to do the converse: to report how long a program takes to finish. In the `Sensing` menu, you will see a command called `reset timer` and a reporter called `timer`:

![](../.gitbook/assets/image%20%28189%29.png)

Activate \(tick-mark\) the `timer` reporter and you should see a timer ticking away in the top left corner.  It's been ticking ever since you opened up Snap_!_ , and counts in tenths of a second:

![](../.gitbook/assets/image%20%28184%29.png)

 We are going to be performing timing experiments in the following sections, so this timer will prove useful.  Add the following timing framework script into the space for Snap_!_ scripts:

![](../.gitbook/assets/image%20%28182%29.png)

The script will reset the timer whenever the green flag is pressed. The sprite will then say `Hello!` for 1 second, and soon after that, the sprite will say the current time, less 1 second to account for how long the sprite said `Hello!`.  If we replace `Hello!` with a reporter, then the sprite will say the answer of the reporter, and one second later, how long the reporter took to generate the answer: this is the timing information that we need.  Save the script with the name `TimingFramework`.

### Do You Have Time to Add?

Let us start our timing experiments with something simple: how long does it take for a computer to add 1 to \(or _increment_\) a number?  Replace `Hello!` in the timing script with an addition operator from the `Operators` menu, and add `1` to `100000` \(that's five zeros!\).  Run the script a few times \(around four\) to get an idea of the average approximate time \(in seconds\) it takes for the computer to increment `100000`. Run the script repeatedly by double-clicking on it; do _not_ place the script inside a `repeat` or a `repeat until` block, since we are interested in knowing the _approximate_ time the script takes to run once.

    Now, pause here and think: what's your gut feeling for how much longer the computer would take if we doubled `100000`?  Test your intuition: Get an average approximate time for how long it takes the computer to increment numbers that you progressively double: `200000`, `400000`, `800000`, and `1600000`.  Remember that for each number, you need to run the timing script multiple times \(around four\) to get an idea of the average approximate time \(you don't have to be precise\).  What do you observe?

    Take another huge leap and find out how long it \(approximately\) takes for the computer to increment numbers that you progressively scale by 10: `160000000`, `1600000000` \(that's eight zeros\), and maybe `16000000000` \(that's nine zeros\).  What do you observe?

