---
layout: page
title: 'Website Programming pt. 1: Intro to HTML'
date: '2020-12-06T17:00:40+00:00'
tags:
- programming
- programming tutorial
- html tutorial
- html
- tutorial
tumblr_url: https://undedinside.tumblr.com/post/636791858974097410/website-programming-pt-1-intro-to-html
---
There are plenty of frameworks that make creating websites but maybe you want to do it yourself. In this series of guides I will teach some of the basics of website programming, starting with HTML.

HTML (HyperText Markup Language) is a simple language, that can be used to make static websites. HTML actually tells the websites visitor how to display a website, meaning that it is up to the user’s browser to actually run the code. It is neither compiled (Like the C family) or interpreted (Like [Python](/tutorials/python-pt-1-intro-to-variables.html) so no fancy compilers or interpreters are needed. You can code a website using Window’s notepad software, but any text editor will do (I personally prefer using <a href="https://notepad-plus-plus.org/">notepad++</a>)

To start writing our website, we will create a file call ‘index.html’. We call the file this because we aim to eventually put our website on a webserver. The software for hosting websites on these servers looks for a file called index to display first.

With our file created, we can now open it with our text editor of choice.

## Let’s Start Coding

<figure class="tmblr-full" data-orig-height="584" data-orig-width="732"><img src="https://64.media.tumblr.com/c67ace694c175be3663c6a5037486972/fa5dbb21dbd78278-2d/s540x810/50dec1bee5aa92733671c8d4f53d435315510f27.png" data-orig-height="584" data-orig-width="732"/></figure>

HTML is written with tags surrounded by &lt; and &gt;, usually with opening and closing tags but not always. The first tag we use is &lt;!DOCTYPE html&gt;. This tag doesn’t affect the look of the website, and isn’t _strictly_ necessary, but it tells the users browser how to show the page and it is good practice to include it. DOCTYPE is a bit strange because you don’t have to close it, read on if that doesn’t make much sense.

After writing that we are using an HTML document, we then declare that the current part of the page we are working on is HTML and we do this with the &lt;html&gt; tag. This tag has to be closed however, so after opening it, you type it again but this time with a / before the name of the tag, like so:

<figure class="tmblr-full" data-orig-height="584" data-orig-width="732"><img src="https://64.media.tumblr.com/370845a46a71a1def42d81aa1a8c8b68/fa5dbb21dbd78278-47/s540x810/568f766ef61505c49fe2fb8d8e1572581d23899d.png" data-orig-height="584" data-orig-width="732"/></figure>

This also isn’t strictly necessary right now, but it’s a good habit to get into for when we start using scripting. From now on all the coding we do will be between these two tags.

Next we can create a heading for our page. This is going to be a nice, big word or phrase to title the page/website. There are six levels of heading: h1 is the biggest, with h6 being the smallest. Like the html tag, this has to be opened and closed, but we will put the text to be displayed between the tags.

<figure class="tmblr-full" data-orig-height="584" data-orig-width="732"><img src="https://64.media.tumblr.com/3e3caa79cef1a8645bb036f6b42c3862/fa5dbb21dbd78278-1c/s540x810/cafb7463be4a19219afdbf39073d2f068b67910d.png" data-orig-height="584" data-orig-width="732"/></figure>

(The indentation on line 3 isn’t necessary and won’t impact the look of the website, but it does help make coding clearer.)

Here I used the classic “Hello, World!” but as this is your website, feel free to use whatever you want. To get some more experience with HTML, feel free to change the size of the heading. Remember to change the size on the closing tag as well.

What does this look like though? Well we can open the page with our browser by clicking on the file in our documents, and it should open.

<figure class="tmblr-full" data-orig-height="1049" data-orig-width="1858"><img src="https://64.media.tumblr.com/da7f28e78387eb74df4593219812a25a/fa5dbb21dbd78278-d3/s540x810/839adade79bb4541ebd3996ca0efdb9eea390f5c.png" data-orig-height="1049" data-orig-width="1858"/></figure>

Here is my site. It’s looking a little bare, so I think I’ll add some text. You can add paragraphs of text using the &lt;p&gt; tag, like this:

<figure class="tmblr-full" data-orig-height="584" data-orig-width="732"><img src="https://64.media.tumblr.com/f010fea4fe7ff5eb9c7265b7d2cd83b3/fa5dbb21dbd78278-fc/s540x810/2eebcdf2c63841c409dadef9bb8b21fa45f6cd5d.png" data-orig-height="584" data-orig-width="732"/></figure>

Viewing it in the browser shows me this:

<figure class="tmblr-full" data-orig-height="1048" data-orig-width="1858"><img src="https://64.media.tumblr.com/596468ba57616c645353c03a8d2c7b20/fa5dbb21dbd78278-28/s540x810/ae50e11d37ac3e90cd14d4a09c5ea74cc582374f.png" data-orig-height="1048" data-orig-width="1858"/></figure>

Now it’s not looking _quite_ so empty. I think that’s all for now. I know it’s still very basic, but it will flesh out as I keep writing these guides.

The code is available on GitHub if you want to download it, and as always you can always reach out to me on Twitter or Tumblr for any questions/suggestions/friendly messages.
