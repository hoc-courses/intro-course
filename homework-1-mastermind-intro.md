# Homework 1: Mastermind Intro

### Description <a id="h.30j0zll"></a>

The goal of this homework assignment is to create the basic infrastructure for the game Mastermind \(a code guessing game between two human players\).  Player 1 provides a secret code and Player 2 tries to guess what it is using feedback she received from previous guesses.

### Gameplay Overview <a id="h.uxd8dvo6gcoz"></a>

1. Player 1 enters the secret code. A secret code is 4 letters long \(no spaces\), where each letter is one of ROYGBV \(the first letters of the standard colors of the game: Red, Orange, Yellow, Green, Blue, Violet\). The secret code may have repeated letters in it. You may assume that Player 1 will enter a valid code: you don’t need to check whether the code is valid or make sure your code works for invalid codes.
2. The secret code is immediately hidden from view.
3. The computer asks Player 2 to guess the code.
4. The computer tells Player 2 if their guess was right or wrong.
5. If their guess was correct, the computer should tell them how many guesses it took the user to get to the correct answer.
6. If their answer was incorrect, the computer tells them the indices of the letters that were correct \(ex: if the secret code is ROYG and Player 2 guesses RBYB, the computer should tell them that letters 1 and 3 were correct\). The computer then asks Player 2 to guess again.

Here is an example of the game. Please make sure that your game follows this general pattern and meets all the requirements listed above. \[The words in brackets are our commentary, the computer does not need to say them\]:

Computer: Welcome, BJC encoder. What is the secret code?

Player 1: RRBG

Computer: Welcome, BJC decoder. Try to guess the code!

Player 2: VBOG

Computer: No, but you have the following slot\(s\) correct: 4

\[G is in the correct position\]

Player 2: OYRO

Computer: No, and none of the slots are correct.

Player 2: RRVG

Computer: No, but you have the following slot\(s\) correct: 1 2 4

\[R, R and G are in the correct position, all the correct slots are given at once\]

Player 2: RRBG

Computer: Yes, that is correct! You figured it out in 4 guesses.

\[...and the game ends\]

### Requirements <a id="h.1fob9te"></a>

You should start from a blank Snap! project. You are required to make the following helper reporter block. Solutions that do not build and use this block will be penalized. Also, please note that this reporter has inputs. You should be giving your block inputs as demonstrated.

You must create and use a helper block called “matching slots” that takes in as input two words, and calculates the slots of the two words that match. All of the correct slots should be returned at once, and your block should behave exactly like the block below:

![](https://lh4.googleusercontent.com/bBI2z8wC9tJiopGzfyaqxQg6-bof3zcJY-qvIZcQzgijRd_GCENh-RRaAs7azliLjITbQFFQnbr_e6734O68GTiCHD1TmLvN2vo92f0DVK9ekHV6H7EfofPNtQSr5_YRGpnygVo)

![](https://lh6.googleusercontent.com/XB0QOvbRrSfSLhR88Pv6u9t5UJJ6LYNmdSxyESXkxR6go0JZ5WdfUBQY6dZtXj9wzmjMKS1T2fF-nYz-4AgFiqCQKS3PgGILDBhARnheYWBjpnhjrcVTgqREww2oA32m0ff7n_U)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Input</th>
      <th style="text-align:left">Output</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>guess: a word representing the user&#x2019;s guess</p>
        <p>secret key: a word representing the secret key</p>
      </td>
      <td style="text-align:left">All slots/positions where the guess and secret key have the same positions</td>
    </tr>
  </tbody>
</table>

There are two general strategies to creating this block: using a word to keep track of the matching slots, or using a list. If you choose to use a word, the mystery block at the bottom of [this page](https://www.google.com/url?q=https://beautyjoy.github.io/bjc-r/cur/programming/functions/reporters.html?topic%3Dberkeley_bjc%252Fintro_pair%252F3-conditionals.topic%26course%3Dcs10_su19.html%26novideo%26noreading%26noassignment&sa=D&source=editors&ust=1628734919213000&usg=AOvVaw01YTiRdQckt-uIXxbQ_Kkb) may be helpful.

If you choose to use lists to build this block, here are some blocks that may be helpful:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Block</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/c2f9GrjfYIa-YdHovSdhSkqP7GQMqFfcrDwOFYbUDu-nTBClrYLfyurecaZnKl8wzd5G99a3pYQiyeFh-u3_idar0q7h0eGwIt51ycOzTBdVGyav75XiyJvA5MkOvP-aeIk0P1A"
        alt/>
      </td>
      <td style="text-align:left">Set a variable called var to an empty list.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh4.googleusercontent.com/N3LcqJX5rsGkGy8rzDmPuZLP9H6TfLc-CME4pEdROllqwc9rgdJVTC6rUtFVnsOG7dIZHM1-aPnLs6QUFlcdLJxNdfSuS5ItiK4ofdR4PPuw9AiSp1SYAmj7phMiPdGuMC1GXpY"
        alt/>
      </td>
      <td style="text-align:left">Add an item called &#x201C;word&#x201D; to the list represented by var.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="https://lh3.googleusercontent.com/xXNFWQpFU0reixRoo8kFeq_FaJ9cftbl_ECbd3b5zHYNy5KrW0-4j3Bd3TQ_Kdvm-jDxZN2HVRIeFDKhygzibYFDE5hSiOVhczBmWNK5O1wGKrFlUu7AiYZnAGxn3niaw3S9LOc"
        alt/>
      </td>
      <td style="text-align:left">
        <p>Turn the list called var into a word. For example, if var is a list of
          1,2,3, this block will output &#x201C;123.&#x201D;</p>
        <p>In order to access this block, you will need to select the &#x201C;file&#x201D;
          icon on the top left corner of Snap!, and then click &#x201C;import tools.&#x201D;</p>
      </td>
    </tr>
  </tbody>
</table>

### Tips <a id="h.2et92p0"></a>

* Take a look at Lab 3 before you begin this homework.
* Save your code often and back it up using a free cloud storage service like DropBox or Google Drive.
* Code a little bit at a time and test as you go.

