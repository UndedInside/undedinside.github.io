---
layout: page
title: 'Linux pt. 4: Finding Files'
date: '2020-12-29T18:07:05+00:00'
tags:
- linux
- linux tutorial
- linux terminal
- linux guides
- linux terminal guide
- Kali
- kali linux
- hacking
- hacking tutorials
- hacking guide
tumblr_url: https://undedinside.tumblr.com/post/638879767328882688/it-happens-to-everyone-you-need-a-certain-file
---
It happens to everyone: You need a certain file for whatever reason, but you just can’t remember where you saved it. If you’re like me organization may not be your forte and it may be easy to lose files, luckily Linux has ways of finding them. The ‘find’ command is very useful for this, but can take a while to learn. It has a variety of uses, but for this guide we’re just going to use it for finding lost files that we can remember the name of.

<figure class="tmblr-full" data-orig-height="558" data-orig-width="911"><img src="https://64.media.tumblr.com/60a454de9de9d05c27eb220f9ba2063e/0cafc52f17a0357b-98/s2048x3072/7ecf78ccdf613537fbf9fe7987ef3df459c7bc7e.png" data-orig-height="558" data-orig-width="911" data-media-key="60a454de9de9d05c27eb220f9ba2063e:0cafc52f17a0357b-98"/></figure>

(Damn it, where did I save my to-do list?)

The ‘find’ command has four main parts. After the command ‘find’, you need to specify which directory to look through, then you can tell the program the type (the find command can locate both files and directories), then the name. I’ll talk about the last bit in a minute.

## Finding a File:

So say I need to find a file called TODO.txt, and I know it’s in my ~/Documents directory. I can use the command ‘find ~/Documents -type f -name TODO.txt’. the ‘-type f’ flag denotes we are looking for a **f**ile, and -name is pretty self-explanatory.

<figure class="tmblr-full" data-orig-height="558" data-orig-width="911"><img src="https://64.media.tumblr.com/7a7cac8cb92950f156ce96a437c82ada/0cafc52f17a0357b-da/s2048x3072/e48e7a37a987bc98d7c2cd3314bfeacdddd3b52e.png" data-orig-height="558" data-orig-width="911" data-media-key="7a7cac8cb92950f156ce96a437c82ada:0cafc52f17a0357b-da"/></figure>

Now I have the path to the file.

<figure class="tmblr-full" data-orig-height="99" data-orig-width="397"><img src="https://64.media.tumblr.com/e60c51957b5b9ffa658a364fc50f4f8b/0cafc52f17a0357b-28/s2048x3072/cc23d981c49e1ab19ede6e988ae9f24375547097.png" data-orig-height="99" data-orig-width="397" data-media-key="e60c51957b5b9ffa658a364fc50f4f8b:0cafc52f17a0357b-28"/></figure>

## Finding a Very Lost File:

What if I don’t know where I saved it at all? Well then when specifying the location you use ‘/’, and the output is less pretty:

<figure class="tmblr-full" data-orig-height="559" data-orig-width="911"><img src="https://64.media.tumblr.com/fdca01f7fffbcbb0aaaa8b33447deadd/0cafc52f17a0357b-24/s2048x3072/0c98eb8f82ffc7ce4ce8e375a05e4e456a98eb81.png" data-orig-height="559" data-orig-width="911" data-media-key="fdca01f7fffbcbb0aaaa8b33447deadd:0cafc52f17a0357b-24"/></figure>

(I don’t think I have the right permissions to access some of these files)

We can see the file here, but sometimes it can be hard to find in the sea of ‘Permission denied’, this is where the trick I mentioned earlier comes into play. There is a file called /dev/null on Linux where anything written to it is lost. By adding 2>/dev/null to the end we send all errors (represented by 2) to /dev/null.

<figure class="tmblr-full" data-orig-height="558" data-orig-width="911"><img src="https://64.media.tumblr.com/2ce1e8ad9546e2015439cd9cfbf2ad51/0cafc52f17a0357b-b6/s2048x3072/9e5052de2c7e9e82594fede1eeae00a9f75aac3e.png" data-orig-height="558" data-orig-width="911" data-media-key="2ce1e8ad9546e2015439cd9cfbf2ad51:0cafc52f17a0357b-b6"/></figure>

(Isn’t that much better?)

## Finding a Directory:

Finding a directory works very similarly to finding a file, but you change the value of the ‘-type’ flag to ‘d’ instead:

<figure class="tmblr-full" data-orig-height="70" data-orig-width="514"><img src="https://64.media.tumblr.com/f9c477a04d7615205ce28659872d4905/0cafc52f17a0357b-a2/s2048x3072/517e1160eb0f3a3114368193a08305929b89a6b8.png" data-orig-height="70" data-orig-width="514" data-media-key="f9c477a04d7615205ce28659872d4905:0cafc52f17a0357b-a2"/></figure>
