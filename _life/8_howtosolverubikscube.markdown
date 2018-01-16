---
layout: post
title: solving a rubik's cube like a pro s
date: 2018-01-04 18:32:00
description: solving a rubik's cube like a pro
comments: true
---

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1589.jpg" >
</figure>

Everyone has played around with a Rubik's cube at some point. You might even have been successful, but if you're anything like me then you would have gotten one side of the cube almost right when you decide to give up and just toss the cube aside.

I have never actually seen someone in real life solve a Rubik's cube until I met my colleague. He is a Rubik's cube World Champion (yes, there is actually such a thing). He holds the 2012 World Record for solving the cube in 26.36s. You can see him in action <a href="https://www.youtube.com/watch?v=mCyYPimImyM">here</a>.

I played around with one of his cubes during a conference while waiting for the next talk. I obviously struggled a lot, but he gave me a few quick pointers that led me to believe that this is actually solvable.

He taught me that the center blocks can't move and that each block has a certain position. So you need to keep the corner block and side colors in mind. This was a revelation. 

I could tell you need a strategy (aka algorithms), some skill, insight and practice. It was not just plain luck. This intrigued me. 

He was kind enough to give me a Rubik's cube for Christmas since I showed some interest at the conference (and because I asked).

The day I received it, I ran home. I had to solve it immediately. 

After watching a few youtube videos, I managed to obtain the algorithm that worked for me. I solved it within 2 days of practicing. 

I found "my" strategy <a href="https://ruwix.com/the-rubiks-cube/how-to-solve-the-rubiks-cube-beginners-method/">here</a>. I will share my interpretation in this post. 

The first step is to become comfortable with the cube. For my strategy, you should always hold the cube as shown in the image above. 

Become familiar with notation. Front, right, up, left and down.

## Notation
<br/>

F: front, R: right, U: up, L: left, D: down

Normal rotations are clockwise.
Counterclockwise rotations are marked with an apostrophe (').

## Strategy
<br/>

### White cross
<br/>

Start off with a white cross. There are no algorithms available here, but it should be fairly easy to get to the result. 

It is important for your cube to resemble the picture. 

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1590.jpg" >
</figure>

### White corners
<br/>

Next up are the white corners. There are 3 algorithms available. Make sure that the side colors resemble a T.

<b>Result</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1594.jpg" >
</figure>

<b>F D F'</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1591.jpg" >
</figure>

<b>R' D' R</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1592.jpg" >
</figure>

<b>R' D2 R D R' D' R</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1593.jpg" >
</figure>


### Second layer
<br/>

The second layer is next. Here we have 2 algorithms. Sometimes you need to do the algorithm twice before your block is in the right position.

<b>Result</b> 

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1597.jpg" >
</figure>

<b>U R U' R' U' F' U F</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1595.jpg" >
</figure>

<b>U' L' U L U F U' F'</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1596.jpg" >
</figure>

### Yellow cross
<br/>

<b>F R U R' U' F'</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1598.jpg" >
</figure>

### Yellow edges
<br/>

The yellow edges need to be positioned in the right place according to the side colors. If you hold the cube as shown in the picture you can exchange the two blocks using the algorithm.

<b>R U R' U R U2 R' U</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1599.jpg" >
</figure>

### Yellow corners on their places
<br/>

Now you have to get the yellow corners on the right places. This step is crucial. Find a piece that's already in the right place like shown in the picture. The colors should be yellow, blue and orange in this case, no matter the orientation.

Angle the block with the correct block as indicated in the picture. Re-do the algorithm until all the other corners are orientated correctly. 

If there is no correct corners initially, then do the algorithm once to obtain one. 

<b>U R U' L' U R' U' L</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1600.jpg" >
</figure>


### Orient yellow corners
<br/>

The final step is to orient the corners. Hold the cube in your hand with an unsolved corner to the front. Do the algorithm twice or four time. 

It might seem as if you're messing up the whole cube, but keep on repeating the algorithm until the corners are in the correct place. Only twist the top row when the next corner needs to be fixed. 

<b>R' D' R D</b>

<figure class="aligner-center">
	<img src="/blog/img/rubix/IMG_1601.jpg" >
</figure>

<br/>
### Success!
<br/>

<hr>
<br/>
## Summary
<br/>

F: front, R: right, U: up, L: left, D: down

Normal rotations are clockwise. Counterclockwise rotations are marked with an apostrophe (‘).

1. <b>White cross</b>
2. <b>White corners</b> 
- F D F'
- R' D' R
- R' D2 R D R' D' R

3. <b>Second layer</b>
- U R U' R' U' F' U F
- U' L' U L U F U' F'

4. <b>Yellow cross</b>
- F R U R' U' F'

5. <b>Yellow edges</b>
- R U R' U R U2 R' U

6. <b>Yellow corners on their places</b>
- U R U' L' U R' U' L

7. <b>Orient yellow corners</b>
- R' D' R D
