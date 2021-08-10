# Snap! - Multiple Broadcasts

This section is to help you understand the machine model some more, so that you don't get frustrated as you're working on your own projects. There are some subtleties when the same message is broadcast multiple times.

Read the following _Snap!_ scripts:

![](../.gitbook/assets/image%20%28224%29.png)

![](../.gitbook/assets/image%20%28221%29.png)

![](../.gitbook/assets/image%20%28174%29.png)

What do you think the list `some list` will look like if we press `b`? What about if we press `w`? Discuss with your neighbor. When you're ready, move on to the next page.

Run the example in _Snap!_ with this [`file`](https://beautyjoy.github.io/bjc-r/prog/Snap/MultipleBroadcastShort.xml). Is the answer what you expected?

Things may not go as planned when multiple messages are being received at once. If you want _all_ of them to take effect, use `broadcast _ and wait`

