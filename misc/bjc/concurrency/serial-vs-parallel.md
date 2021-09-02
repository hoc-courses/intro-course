# Serial vs Parallel

When you put two "When green flag ..." hat blocks in the same sprite, both will run at the same time! Similarly, if multiple sprites all have "When green flag..." hat blocks, these will run concurrently as well.

Open this Snap_!_ file [SerialVsParallel](https://beautyjoy.github.io/bjc-r/prog/Snap/SerialVsParallel.xml), and click the green flag \(not the block in the default sprite!\). Two things will get drawn:

* You will see one 'serial' gold square sprite \(ten pixels on a side\) paint the area on the right by stamping itself.
* You will also see two blue 'parallel' 10x10 sprites sharing the labor of painting the area on the left by stamping themselves.

\(Two screenshots are included below\) Note that the parallel side finished in exactly half the time of the serial side. Discuss with your partner why this is. You should use the phrase **time sharing** in your explanation. If you don't remember what that is, go back to the first page of lab, "_Snap!_ Machine Concepts"

First, a screenshot taken during computation.

![](../../../.gitbook/assets/image%20%28311%29.png)

Second, a screenshot taken after computation has finished.

![](../../../.gitbook/assets/image%20%28285%29.png)

It is important to form an accurate mental model of the machine/software when working with it. Hopefully you have seen here that Snap_!_ gives equal time to all the workers \(scripts\), in lock step, and that concurrency bugs can creep up very easily.

### 

