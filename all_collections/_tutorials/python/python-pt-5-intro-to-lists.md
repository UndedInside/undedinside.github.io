---
layout: page
title: 'Python Programming pt.5: Introduction to Lists'
date: '2021-02-18T14:56:24+00:00'
tags:
- coding
- programming
- coding tutorial
- programming tutorial
- linux
- linux tutorial
- linux terminal
- hacking
- hacking tutorials
- hacking guide
tumblr_url: https://undedinside.tumblr.com/post/643488215846862848/python-programming-pt5-introduction-to-lists-if
---
If you have an amount of data you want to group together, how would you do it? One method might be a series of variable assignments. A shopping list might look like this:

<figure data-orig-width="357" data-orig-height="65" class="tmblr-full"><img src="https://64.media.tumblr.com/0e32cabbdeee00b8a7af253ed0e07162/e7ad5b22e00ad663-0d/s540x810/49f12c7952bf22ac88f08f896a0babbd21e61de7.png" alt="image" data-orig-width="357" data-orig-height="65"/></figure>

This has some problems though, mainly that you have to work with each variable manually in the code. If you want to print all items on your shopping list, then you must use a print statement for each item. To print a certain item, you need to code a print statement to print that specific item. This approach may work for a small shopping list but becomes impractical for longer ones. Most programming languages have data types called “arrays” and “lists” to help you work with these collections of data, and in this guide, I’m going to teach you how to work with lists in python.

The first thing you need to know is how to define a list in python. Lists are assigned like any other variables, but the values are put between square brackets with each item separated by a comma.

The same shopping list can be implemented like this:

<figure data-orig-width="384" data-orig-height="34" class="tmblr-full"><img src="https://64.media.tumblr.com/600ca38b1adc244ba62faa0c4d6129b8/e7ad5b22e00ad663-fc/s540x810/04a13927b5583edf46526a3c0c3a88e23d6e94e3.png" alt="image" data-orig-width="384" data-orig-height="34"/></figure>

Not only have the number of lines of code been reduced, but we can now work programmatically with our list. The most fundamental thing about lists is that every item has an ‘index’, which describes its location in the list. This location starts counting from 0, so the first item is index 0, with the second item being index 1, etc. You can access an item in the array with its index number.

<figure data-orig-width="482" data-orig-height="115" class="tmblr-full"><img src="https://64.media.tumblr.com/69825c3e05b0b23a9fe4ffed2a64bcfb/e7ad5b22e00ad663-9b/s540x810/0c9cbc52004a1cef84840a53654425ea985a90c7.png" alt="image" data-orig-width="482" data-orig-height="115"/></figure>

You can also overwrite an item of a list by assigning that index of the list to a new value.

<figure data-orig-width="490" data-orig-height="52" class="tmblr-full"><img src="https://64.media.tumblr.com/6966412b6b56532b33a10dfb94f496f9/e7ad5b22e00ad663-ce/s540x810/dfa12b06a4308a4cf026cb6890cf51cf9564c7d0.png" alt="image" data-orig-width="490" data-orig-height="52"/></figure>

There are many tricks you can do with list indexes, which can be found <a href="https://www.w3schools.com/python/gloss_python_access_list_items.asp">here</a>.

This is all well and good for modifying existing items, but what about adding more items? The main way this is done is with the append method, which adds an item to the end of the list.

<figure data-orig-width="239" data-orig-height="53"><img src="https://64.media.tumblr.com/010842f9c3cb192e192191ef8b06999a/e7ad5b22e00ad663-1c/s540x810/39be337bfcd95b49087a9aa71646cfebf876050e.png" alt="image" data-orig-width="239" data-orig-height="53"/></figure>

There are two methods for removing items from a python list. The pop method removes an item from a certain index, while the remove method removes an item that matches the value it is given.

<figure data-orig-width="418" data-orig-height="115" class="tmblr-full"><img src="https://64.media.tumblr.com/e6957b670b7044f0a355361ff8deb04e/e7ad5b22e00ad663-da/s540x810/06374f8d93fa052c3f4652a1ed531c9b71f95d83.png" alt="image" data-orig-width="418" data-orig-height="115"/></figure>

I hope you have been able to follow along with this tutorial. I have written code snippets showing each of these features which is available to download from <a href="https://github.com/UndedInside/CodeExamples">this</a> github repo. Feel free to play about with it or even write your own code to see how lists work.

This post was just an introduction. In my next post I will show you some practical examples of working with lists.
