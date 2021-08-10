# Determinism vs Non-determinism

Snap! supports parallelism! Let's explore some of the fun/challenges of concurrent programming, nondeterminism. In this context, this means we cannot pre-determine what the results will be; determinism means we could predict what the outputs would be.

In the last Snap_!_ exercise, it was a little artificial; the sprites were in lock step. Let's take a look at a similar project, [`Determinism`](https://beautyjoy.github.io/bjc-r/prog/Snap/Determinism.xml). Here, four 60x60 sprites do the same thing \(color the screen by stamping themselves through the `Fill Screen` command shown below\), and once they finish, they add their name to the end of the `finish` variable. Run it a couple of times. Boring, right? That was because Snap_!_ is still in lock step.

Make a very small change to Fill Screen - have each sprite wait a random value between 1 and 1/10 seconds before stamping. \(this involves the introduction of a very simple command right before the "stamp" call in `Fill Screen`: "wait \(1 / \(pick random \[1\] to \[10\]\)\) secs"\). Run it a few times; now what happens? \(Answer: Four "threads" take off, and the slowest \(i.e., last\) color at each time step is that one who colors that 60x60 square\). Save this project as a Snap_!_ file called `NonDeterminism.xml`.

![](../.gitbook/assets/image%20%28166%29.png)

### What are the Possible Values?

If we run the following Snap_!_ code, we'll see that `result` variable will have different values each time. Try to predict the all the possible values. If you're stuck, just move on to the next page, where we'll try out some experiments.

![](https://beautyjoy.github.io/bjc-r/img/lab-9/subset-race-main.png)

![](../.gitbook/assets/image%20%2886%29.png)

![](../.gitbook/assets/image%20%2892%29.png)

![](../.gitbook/assets/image%20%28261%29.png)

![](../.gitbook/assets/image%20%2857%29.png)

### These are the Possible Values

Play around with the script first: [`Race`](https://beautyjoy.github.io/bjc-r/prog/Snap/SubsetRace.xml).

The answer is: all the permutations of a,b,c where all three letters are present \(there are six of them\) + all the permutations of a,b,c where only two letters are present \(also six of these\) + all the permutations of a,b,c where only one letter is present \(three possibilities\) for a total of fifteen possibilities.

* If all three letters are present, it is as if we were deterministic \(didn't have random wait times\). Here is how it could happen \(for this example order, all 6 permutations are possible = {abc, acb, bac, bca, cab, bca}\):
  * result starts empty
  * a, b, and c all clear result.
  * a reads result \(\), joins its a, result is now a.
  * b reads result \(a\), joins its b, result is now ab.
  * c reads result \(ab\), joins its c, result is now abc.
  * finish is abc
* If only two letters were present, we had a race condition, and here is how it could happen \(again, all 6 combinations and permutations are possible = {ab, ba, ac, ca, bc, cb}\):
  * result starts empty
  * a clears result \(\)
  * a reads result \(\), joins its a, result is now a.
  * b and c clear result.
  * b reads result \(\), joins its b, result is now b.
  * c reads result \(b\), joins its c, result is now bc.
  * finish is bc
* If only one number were present, we also had a race condition, and here is how it could happen \(again, all permutations possible = {a, b, c}\):
  * result starts empty
  * a, b clear result.
  * a reads result \(\), joins its a, result is now a.
  * b reads result \(a\), joins its b, result is now b.
  * c clears result.
  * c reads result \(\), joins its c, result is now c.
  * finish is c

