# Testing 2048

Let's now turn to some tests of the blocks that we provided for 2048. Click on the "2048 Lab" sprite, and you should see a test that looks like this at the top:

![](../.gitbook/assets/image%20%28147%29.png)

This block ensures that "size of board" applied to "new board of size 10" returns 10. If you click that block, you should see "true," since this test passes. This tells us that these two functions have consistent behavior with each other, which is a good thing!

The next test should look like:

![](../.gitbook/assets/image%20%28158%29.png)

This test is a little trickier. Since we're testing a command block, we have to create a temporary variable to use that command block. In this case, the test verifies that if you set position \(1, 4\) to 2, that the actual value stored at that position is a 2. It also verifies that the value at position \(1, 2\) is just zero \(since it hasn't been set\). Again, if you run this test, you should get back `true` twice. Make sure that this test makes sense before proceeding.

