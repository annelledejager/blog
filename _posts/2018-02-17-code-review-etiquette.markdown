---
layout: post
title:  code review etiquette
date:   2018-02-17 08:46:00
description: code reviews do's and dont's for a healthy software team environment
comments: true
---
The purpose of code reviews are to catch mistakes made during the initial implementation phase and to improve the quality of the software. It also helps the younger developers to improve and gain confidence. 

There's always that one developer that you always ask for reviews- the "easy approver". They are easily pleased and your code is usually approved instantly. On the other hand there's always that developer that you dread asking for a review - the virtually "impossible approver". This developer will comment and fight you on everything. The implementation will usually take a third of the whole development time due to this long back and forth review.

In my experience neither of the two developers` code review approaches are constructive towards the developer under review or their code. 

Code reviews can be helpful or destructive and toxic. This post summarizes the do's and dont's for a healthy software team environment as described in <a href="https://medium.com/@sandya.sankarram/unlearning-toxic-behaviors-in-a-code-review-culture-b7c295452a3c">Unlearning Toxic Behaviors in a Code Review Culture</a> by Sandya Sankarram.

## The dont's
<br/>
 * <b>don’t pass opinion off as fact</b>
 
 * <b>don’t overwhelm with avalanche of comments</b>
 <br/>
 Don't comment E.g `extra space` multiple times. This will pollute the review and come across as nitpicking.

 * <b>don’t ask engineers to solve problems they didn’t cause “while they are at it”

 * <b>don’t ask judgmental questions</b>
<blockquote>
 Why didn’t you just do ___ here?”
 </blockquote>

 * <b>don’t be sarcastic</b>
<blockquote>
Did you even test this code before you checked it in?
</blockquote>

 * <b>respond to every comment</b>
 <br/>
 If you're asking someone to review your code then its disrespectful to not reply to every comment. It will leave the reviewer thinking why did they even bother reviewing your code.

 * <b>don’t ignore toxic behaviors from high performers</b>

 * <b>don’t make people feel bad that they “should already have known” this piece of info</b>

## The do's
<br/>
 * <b>use questions or recommendations to drive dialog</b>
 
 * <b>collaborate, don’t back-seat drive</b>
 <br/>
 In my experience and in our team we find it constructive to sit with the reviewer while he/she reviews your code. You open a dialog by doing this. The issues are addressed, discussed and resolved faster. 
 
 * <b>know when to take a discussion offline</b>
 
 * <b>use opportunities to teach and don’t show off</b>
 
 * <b>automate what can be</b>
 <br/>
 E.g use a linter
 
 * <b>refuse to normalize toxic behavior</b>
 
 * <b>set the standard as your team is small and growing</b>
 
 * <b>understand you might be part of the problem</b>
 <br/>
 Don't simply point out a bug, because you've managed to identify it. This mindset could lead to showing off.
