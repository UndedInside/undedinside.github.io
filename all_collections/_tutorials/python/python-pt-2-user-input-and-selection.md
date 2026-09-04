---
layout: page
title: 'Python Programming pt. 2: User Input and Selection'
date: '2020-11-23T13:00:17+00:00'
tags: []
tumblr_url: https://undedinside.tumblr.com/post/635598974057938944/python-programming-pt-2-user-input-and-selection
---
In the last lesson I explained how to define and output variables. In this tutorial I will teach how to get input from a user and how to make decisions in the code.

To get user input in python you define a variable, but instead of giving it a value, you use an input statement. Inside the brackets of the input statement, you can enter some text to prompt the user into entering input.

To do this we will use an ‘if’ statement. If statements change what code runs depending on whether a condition is met.

<figure data-orig-width="295" data-orig-height="85"><img src="https://64.media.tumblr.com/5692e5981c604e92dfb76cc1019d75d3/fc08ba4975a47d58-dc/s540x810/d7a52e9286695f4199bddc651796421e2450434c.png" alt="image" data-orig-width="295" data-orig-height="85"/></figure>

In this example, print(”Hello, name”) will run if the name entered is Unded (Obviously you can change this to your own name), but if it isn’t the program runs print(”Nice to meet you”, name) instead.

There are three important things to remember with if statements. The first is a note about equals signs in python. One ‘=‘ is used to assign values to variables, while “==“ is used to compare if two values are the same. Trying to use ‘if name = “Unded”:‘ won’t work.

The second thing to remember is the colon. Certain statements like ‘if’ and ‘else’ in python require a colon at the end. If you forget, the code will throw an error and refuse to run.

Thirdly, lines included in statements requiring colons need to be ‘indented’ to tell python that they are a part of that ‘block’ (what I like to call them, I’m not sure of their technical name). Any code included in the ‘if’ or ‘else’ statement needs to be offset from the left of the screen - usually by either tab or 4 spaces. This indicates that code should be run when that condition is met, and can lead to either outright errors or unexpected behaviour, but you’ll see more of how this should look as I write more tutorials.

In this tutorial I have discussed comparing strings, but the principle is the same. You’ll see selection in more depth over time, but this lesson is a good first introduction.
