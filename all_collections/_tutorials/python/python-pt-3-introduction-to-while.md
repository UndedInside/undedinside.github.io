---
layout: page
title: 'Python Programming pt. 3: An Introduction to While Loops'
date: '2020-11-24T17:01:06+00:00'
tags:
- python
- python tutorial
- programming
- programming tutorial
- coding
tumblr_url: https://undedinside.tumblr.com/post/635704722149507072/python-programming-pt-3-an-introduction-to-while
---
While loops are one method of iteration (repeating instructions). As the name suggests, while loops will continue to loop while a condition is met. Let’s start by simply counting to ten.

First we need to define a variable to store the current number and give it a value of 1. We will then loop while our count is less than 10, however we need to be careful here. If we want our count to include the number 10 we need to use ‘&lt;=‘ (less than or equal to) instead of ‘==‘. Using ‘==‘ will stop our count at 9. We also need to remember to _increment_ (increase) count, or else the loop will never end. We could use ‘count = count + 1′ to assign count the value of 1 added to itself, but a more ‘Pythonic’ way of doing that is to use ‘count +=1′. They both do the same thing, but the later is generally considered the more readable way to increment variables.

<figure data-orig-width="344" data-orig-height="121" class="tmblr-full"><img src="https://64.media.tumblr.com/273563988a0be159198762724ee78bf4/2cb40596dcc53243-28/s540x810/946e967168cd3c688cdd2f0140384e30c3534718.png" alt="image" data-orig-width="344" data-orig-height="121"/></figure>

You can see the colon and indentation I discussed in my previous tutorial. That tells the python interpreter that ‘print(count)’ and ‘count +=1′ are to be repeated every time the code iterates through the while loop.

I think a good way to learn is to play around with the code and see how it changes, so here are some suggested changes you can make:
- Change what value is initially given to count
- Change the value of count in the ‘while’ statement
- Replace &lt;= with ==
- Switch the print statement and the incrementing of count

Try and figure out why each of those has the effect it does. They may not seem like important changes, but they can make a big difference and later on they could be the reason for the bug you’ve spent hours trying to fix.
