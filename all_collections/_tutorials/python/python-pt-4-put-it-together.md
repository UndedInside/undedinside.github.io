---
layout: page
title: 'Python Programming pt. 4: Put it Together.'
date: '2020-11-26T17:00:37+00:00'
tags:
- python
- python tutorial
- programming
- programming tutorial
tumblr_url: https://undedinside.tumblr.com/post/635885885748068353/python-programming-pt-4-put-it-together
---
In my [first python tutorial](/tutorials/python-pt-1-intro-to-variables.html) I taught you how to declare variables, [in the second](/tutorials/python-pt-2-user-input-and-selection.html) I taught you selection, and [in the third](/tutorials/python-pt-3-introduction-to-while.html) I taught you while loops. Let’s put these together now to create a simple login program.

This script will give the user three chances to enter the password. If the user gets it right it will welcome them, and will tell the user if they get it wrong.

<figure data-orig-width="424" data-orig-height="167" class="tmblr-full"><img src="https://64.media.tumblr.com/79af8a1255af51a6e7e8a552427cf427/65de4e71df305c6c-18/s540x810/95e99835408463ca4541863b215ccb97dd93aeac.png" alt="image" data-orig-width="424" data-orig-height="167"/></figure>

The first thing we do is declare a variable ‘count’ with a value of 0. This variable will keep a count of how many guesses the user has had.

After that we loop while count is less than 3. Less than (&lt;) is non-inclusive, which means it doesn’t include the number that our variable is being compared to. The while loop will execute if count is 0, 1, or 2.

On the next line we ask for input from the user, and save that in a variable userPass. We then compare userPass with our password. If userPass is the same as (==) “UndedIs1337″ then “Welcome Unded” is shown, and the _break_ statement runs, otherwise it will tell the user they got it wrong and add 1 to count.

I didn’t discuss breaks when I taught about while loops. A break simply stops the loop. The condition of the while loop doesn’t have to be met - the break just breaks the loop instantly.

Changes you could make:
- Change the number count starts at.
- Increase the number count increments to in the while statement.
- Change the password.
- Change the output.

You now have an idea about the very basics of python. There is plenty more that I will go into, as well as revisiting these basics to ensure that you have a solid understanding of it.

As always, if you have any questions, corrections, or comments feel free to leave a note, send me a message, or get in touch with me over twitter <a href="http://twitter.com/UndedInside">@UndedInside</a>
