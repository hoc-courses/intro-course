# Concurrency

## Big Ideas

* Understand the basic components of any computer
* Understand Moore's Law impact on the development of the processors
* Understand parallelism and its limitations in computing
* Explore the history and development of encryption techniques

## Activities

In Snap_!_ what are the issues/facilities to do parallel work, and how does the machine work?

* A single sprite has control blocks which appear to respond in parallel \(e.g., multiple "when green flag, do...", "when space is clicked, do...", "when I receive broadcast", etc.\)
* Multiple sprites only exacerbate the problem, and race conditions could occur \(e.g., what if multiple sprites tried to paint the screen their color all at the same time?\)
* When we call "launch", does that mean another worker starts up? \(answer: yes and no\)
* The meta learning goal for this part is for you to develop an accurate mental model of how Scratch handles concurrency. This is so you avoid race conditions and deadlock, and so that you can fully exploit it to your benefit!

