# Magic Squares

### Getting Started

In this lab, you will write ![green predicate: is a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/isamagicsquare_block.png) that reports whether or not a set of numbers forms a _magic square_. In a magic square, the sum of the numbers in each row, column, and diagonal must be equal.

The data in this list: ![square\_12,13,14,10,18,11,17,15,16](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/square_12_13_14.png) corresponds to this 3-by-3 grid of numbers:  
![square\_12,13,14,10,18,11,17,15,16](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/magic_square.png)

Your report will need to return the correct value for input such as the following:

1. ![is 12,13,14,10,18,11,17,15,16 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is12_13_14magic.png)
2. ![is 80,10,60,30,50,70,40,90,20 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is80_10_60magic.png)
3. ![is 17,16,21,22,18,14,15,20,19 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is17_16_21magic.png)
4. ![is 10,10,10,10,10,10,10,10,10 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is10_10_10magic.png)

Now that you've had some experience deciding what makes something a magic square, it's time to write an algorithm.

1. Using as much detail as possible, you and your partner should _each_ write down—in words, not in code—an algorithm that you can use to decide whether or not a list of 9 numbers forms a magic square.
2. Exchange your algorithm with your partner. Follow your partner's algorithm on this list: ![square\_3,2,1,1,3,2,2,1,3](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/square_3_2_1.png)
3. Discuss any improvements or clarifications needed to make your algorithms as clear as possible.

### Lookup items block

One of the things that will be useful when you write `is _ a magic square?` is a reporter that picks off elements from a given list, like the first, fourth, and seventh element.

Make a red block, ![red reporter: lookup items \(\) from \(\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/lookup_block.png). Here's how it starts:  
![lookup items \(item numbers\) from \(this list\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/lookup_block_def.png)

And here it is in action:

![lookup items \(1,4,7\) from \(nouns\) = \(a,b,c,d,e,f,g,h,i\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/lookup_result1.png)

### Triples

There are several possible algorithms for checking to see if a list forms a magic square. Though the details might be different, your algorithm probably involved identifying three numbers at a time and adding them. Call these sets of three numbers "triples".

![](../.gitbook/assets/image%20%28361%29.png)

 Write a block that finds the sum of the middle row of ![{12, 13, 14, 10, 18, 11, 17, 15, 16}](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/square_12_13_14.png)

Write a block that compares the sum of the middle row and the sum of the right column. Are they equal?

Discuss how you might write a program that compares all of the sums necessary for checking a magic square.

### Finding Triples

How many triples do you have to check to see if a list is a magic square?

 Make a list of lists, called `triple positions` that keeps track of the _positions_ of the triples. Here's a start. The first item, the list \(1, 4, 7\) is identifying the _left column_ in a 3-by-3 grid.  
![list that gives first triple \(1,4,7\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/magic_start_triples.png)

 `Triple positions` gives a list of the positions of the triples. Now make a red reporter block, called `triples in square ()` that returns the _numbers_ from the potential magic square that are in those positions. Here's the beginning of `triples in square ()`.  
![red reporter: triples in square \(square\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/magic_triples_square.png)  
Here's the beginning of the output for the square shown above:  
![triples in square \(12, 13, 14, etc\) = \(12, 10, 17\)](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/magic_firsttriples.png)

Discuss how you can use this information to determine whether the original 9 numbers form a magic square.

### Pulling it all Together

 Make the `Is a magic square?` block.

![](../.gitbook/assets/image%20%28352%29.png)

 Here are some magic squares to test \(from Getting Started\):  
![is 12,13,14,10,18,11,17,15,16 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is12_13_14magic.png)  
![is 80,10,60,30,50,70,40,90,20 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is80_10_60magic.png)  
![is 17,16,21,22,18,14,15,20,19 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is17_16_21magic.png)  
![is 10,10,10,10,10,10,10,10,10 a magic square?](https://bjc.edc.org/Sept2015/bjc-r/img/3-lists/is10_10_10magic.png)

### Extra Challenge

Build a magic square checker for n-by-n squares

