# Concurrency in Snap!



Snap_!_ supports parallelism! The programming environment is full of concurrency, implicit \(two scripts both start when the green flag is clicked, or when they receive the same broadcast message\), and explicit \(the launch block\). Let's first explore the explicit kind, then we will play with the implicit kind a bit.

Let's try to use concurrency for what it was meant for: **speed!**

There are three important models of the machine you should develop:

1. Snap_!_ is like a parent with lots of kids, the parent wants to give the kids equal attention. So if there are 3 things happening at one time, Snap_!_ will rotate among the three of them, giving each of them a chance to do their "thing" \(e.g., complete one iteration of a loop\). It will choose the same order every time, in a very predictable way. This is known as **time-sharing.**
2. Snap_!_ has a **speed governor** so that projects can run at the same speed on different machines. It is obvious why that is important—imagine developing this great Pac Man game on your parent's slow computer and working very hard to get the timing just right so it is not too fast or slow. However, when you share it with others who have faster machines, it runs too fast to play \(because the other computers have a faster "heartbeat", the clock rate\). So Snap_!_ slows itself down on faster computers so that it always looks like it is running on the same, slow, computer. The reason this is relevant in the discussion of concurrency is that \(on the vast majority of computers\) Snap_!_ spends a lot of time just sitting there, waiting, so it has lots of idle "cycles" to handle multiple things running at the same time.
3. Snap_!_ actually does NOT make use of more than one core \(independent hardware computation unit\), it runs everything in **one core** and time shares any parallel task on the single core. This gives Snap_!_ much more control over its parallelism, since once you decide to use two \(or more\) physical cores, you can no longer control when \(or in what order\) the computations will return, and you open up the standard Pandora's box of concurrency problems, like deadlock and race conditions. So your Snap_!_ programs are insulated from these realities, allowing you to have predictable parallelism \(usually impossible\) at the cost of being able to run really fast and make use of hardware resources.

### Try it out

![](../.gitbook/assets/image%20%2895%29.png) ![](../.gitbook/assets/image%20%2897%29.png) ![](../.gitbook/assets/image%20%2864%29.png) 

First, to understand the idea of two things happening at once, download and open this Snap_!_ file [`LaunchTutorial`](https://beautyjoy.github.io/bjc-r/prog/Snap/LaunchTutorial.xml) \(shown above\). After you click the green flag, let it run for a bit, then hit the space bar once. Then hit it again, and again. Talk with your partner about what is happening, and why.

\(Answer: When you hit the green flag, the sprite starts off running in a circle, because it is moving and turning at the same time. Now, whenever you hit the space key the sprite's circles become wider because it is moving _more_ than before, and it only does that because its MOVE _threads_ are increasing, not the number of steps per single move. For example, Snap_!_ initially gives equal time to its 2 "forever" children -- one that turns and one that moves 5 steps. So it is move, turn, move, turn, etc., yielding a \(360/15 =\) 24-sided polygon with 5-step sides. The next time space bar is pressed, another "child" is born, so now the three equal-time children are: "turn", "move" and "move", yielding a 24-sided polygon with 10-step sides, or a "circle" of twice the size.\)

