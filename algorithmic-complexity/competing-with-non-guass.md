# Competing with Non-Guass

We would like to add all the numbers from `1` to `N`, where `N` could be a big number. The obvious way to do this is to simply add them up, one by one.

![](../.gitbook/assets/image%20%28185%29.png)

We can, however, also follow in the footsteps of the young Johann Carl Friedrich Gauss, a now-revered 18th century mathematician. As the story goes, he was punished by his elementary school teacher to do the same exercise: add all the numbers from `1` to `100`. The teacher, J. G. Büttner, assumed that the problem would take Gauss a long time to do, yet Gauss finished the problem in a matter of seconds. 

He realized that, adding `1 + 2 + 3 + ... + 100` was the same as adding `(1 + 100) + (2 + 99) + (3 + 98) + ... + (50 + 51)`. Each pair summed up to `101`, and there were `50` of these pairs, so he quickly deduced that the answer was  `101 × 50 = 5050`. Presumably, teacher Büttner wasn't pleased.

In general, if you wanted to add the numbers from `1` to `N`, the answer would be  
     `(N + 1) × (N ÷ 2)`,  
because there are `(N ÷ 2)` pairs, each of which add up to `(N + 1)`.

Imagine that you are playing a game against young Gauss to see who could add numbers from `1` to `N` faster: he does it his way, while you manually add them one by one. You can either win, lose, or tie in this game. What do you think would happen if `N` is `2`? If `N` is `10`? If `N` is `100`? If `N` is one million?

