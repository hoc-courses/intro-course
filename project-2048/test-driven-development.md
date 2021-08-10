# Test-driven Development

One interesting programming practice is so-called _Test Driven Development_ or [TDD](http://en.wikipedia.org/wiki/Test-driven_development). In TDD, a programmer writes a test for each block _before_ even writing that block at all. A substantial minority of programmers prefer to program in this way. To get a feeling for what it's all about, let's try it for this lab.

There are two main goals for practicing TDD:

* Think _before_ you code. To be able to write a successful test, you need to know exactly what you want your blocks to do. In reality, this exercise takes quite a bit of practice to get used to, but the planning pays off for most programmers who use TDD.
* Make sure you know your code works! In "traditional" programming, where you write tests for code _after_ you finished a block, it's easy to forget writing the tests. TDD helps by making sure you always have a set of test you can quickly run to make sure there are no errors.

Let's start by writing a test for the `merge up` block. In this case, we'll type in all of the values of the board. To make this easier, we've created a `new 4x4 board with values` block that you can use. Each set of four values between `/` symbols is a single row. Try it out with the `update display` block if you are still confused about how this block constructs a new board.

**For You To Do:**

Fill in the output values so that the test pictured below is correct. Note that if you click on the block, it will return `false`. This is because you haven't filled-in the `merge up` block yet! In a sense, you've now created a little game for yourself that you win once the block starts returning true. One of the appeals of Test Driven Development is setting little challenges like this, and basking in the brilliant glow of the `true` that shines forth once your block is properly working.

Once you finish writing a test for an unfinished block you should always verify that the test actually returns `false`. That might seem silly, but it provides a sanity check that the test itself is doing its job. It turns out that it's just as easy to write buggy tests, as it is to write buggy code. A test case that can never fail is not very helpful! By having test cases change from failing to passing, you can verify that both your code and your tests are progressing in sync with one another.

Another advantage of failing tests is that it gives you reassurance that the test is doing it's job. It turns out that it's just as easy to write buggy tests, as it is to write buggy code. A test case that can never fail is not very helpful! By having test cases change from failing to passing, you can verify that both your code and your tests are progressing in sync with one another.

![](../.gitbook/assets/image%20%28234%29.png)

**For You To Do:**

As the final step in this short lab, write a test for the ![](../.gitbook/assets/image%20%286%29.png) ****block. You should have at least TWO boards as input test cases \(whereas our test for rotate clockwise only tried out one input board\). Make sure you have your lab TA check off your test before you leave.

