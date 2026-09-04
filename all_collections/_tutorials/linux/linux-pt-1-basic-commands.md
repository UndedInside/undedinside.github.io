---
layout: page
title: 'Linux Commands pt 1: Directory Traversal and File Creation/Deletion'
date: '2020-08-18T12:01:08+00:00'
tags:
- hacking
- pentesting
- kali
- linux
- linux guides
- hacking guide
- linux terminal
- linux terminal guide
tumblr_url: https://undedinside.tumblr.com/post/626803572762378240/linux-commands
---
This is a quick crash course on some of the basic Linux commands to enable you to use the terminal. We will be using a Kali Virtual Machine for this (for a guide on how to set up a VM, see my earlier posts on the topic)

The first thing you should know about is the prompt. By default the prompt tells you the current signed-in user, the hostname of the computer, and the current directory (We’ll discuss this further later). On Kali it will look like this:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/5587c9fa53f8f83f56979df4b7fd746c/4f4f6e4f74f0ec87-4f/s540x810/a2ca52be50abd1a91ed6c8ed508a7195ff44f355.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

It is formatted as ‘user@hostname:dir$’

This is a little confusing as by default both the username and hostname is ‘Kali’, but it is telling us we are signed in as ‘Kali’, the hostname is ‘Kali’, and the ‘~’ tells us we are in our current home directory.

The first command is “ls”. This command lists all the files and directories in the current directory (’directory’ is a synonym to what are commonly referred to as ‘folders’ in the windows GUI). A standard home directory will look something like this:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/b21419d8f814b9872a8e9b578c317556/4f4f6e4f74f0ec87-93/s540x810/be53b072701a6012437791ccb3a8851f82654b9d.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

We use the command ‘cd’ to Change Directory. Let’s change to the ‘Documents’ dir with the command ‘cd Documents’. You should have noticed how the last part of the prompt has changed to ~/Documents. If we use ‘ls’ we should see that nothing happens.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/5f77a928fcbe1f45051e5bef9b0bc07a/4f4f6e4f74f0ec87-ae/s540x810/d99cb6ec40f1a32ec8720dd74a986e3d5f18eeec.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure><p>

This is because the current directory is empty. Many commands have extra options called ‘flags’ which allow you to change how the command runs. One of the flags for ‘ls’ is ‘-a’, which outputs everything in the current directory including hidden documents and directories. To use these options we type the command, and then the flag.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/f8bf6151420583308e75dfd69a335bd9/4f4f6e4f74f0ec87-c5/s540x810/9861cac5ebcdc3ff6b7692ce6cdae1624e1f1d5a.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

Here you can see there are actually two directories in ~/Documents/, these being ‘.’ and ‘..’. In Linux, the ‘.’ directory is the current directory, and ‘..’ is the directory above it. We can ‘cd’ to these directories like any other.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/c5194475ec810dd119317ddcd1b15a79/4f4f6e4f74f0ec87-0d/s540x810/b90367894a551fe2bf85b9000a4aafbdb47cdc77.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

As you can see, ‘cd .’ didn’t do anything because we were trying to change to the directory we were already in, but ‘cd ..’ took us to our home directory.

It’s looking a bit empty, so let’s learn how to create, see, and edit files.

To create an empty file, we use the command ‘touch [file name]’, so to create a file called ‘hello.txt’ we use the command ‘touch hello.txt’. Let’s cd back to Documents and then try creating a new file.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/f174504e7e6201aec96bd999539c1906/4f4f6e4f74f0ec87-82/s540x810/33c45ed39630e2f9763874cfac50d208e953690f.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

hello.txt has been created. To view files in the terminal, we use the command ‘cat’ (so called because of it’s ability to con_cat_enate files).

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/8ed603c683f487ec10428c1c9cd5364b/4f4f6e4f74f0ec87-88/s540x810/a6f6e576c8d6996a2ba0c7162490ad1fc92ed923.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

Nothing happened because the file was empty, so now we can use a text editor to edit the file. Linux comes preloaded with some text editors. Personally I prefer Nano but there are others to choose from.

After typing ‘nano hello.txt’, nano opens the file like this:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/cfd419fbd3b15dba0ab74fc3cf52d00e/4f4f6e4f74f0ec87-ba/s540x810/affdf981c9e6d165e4ce3681ba4975ad26aaa0aa.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

Feel free to type whatever you want here.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/9948d06f231c3cbb3b225b4d355286a8/4f4f6e4f74f0ec87-18/s540x810/2967d706d9e33a2770d1af6ee78111f0fc3c22b0.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

To exit nano we type Control X:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/591a6ebd9e22e88ab13750528a4e87b5/4f4f6e4f74f0ec87-d8/s540x810/f21459dc0f5084176a3a6dcace6338ab83f490ac.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

then y:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/b357c32fc8a8d4d5a2d0a891c27efba4/4f4f6e4f74f0ec87-02/s540x810/7915931265af6f6cdffc7d2013bdece7f1fc35ca.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

and then enter:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/a0ed6e127f5ee4d763f891c9f7c1ee92/4f4f6e4f74f0ec87-c7/s540x810/f1bedbe23dcbaec9ee8e9148e640540d9ff128fd.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

Now if we type ‘cat hello.txt’, it will output what we wrote.

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/428eb99440d51bf54e976699f2e5b2fa/4f4f6e4f74f0ec87-0a/s540x810/accdf1e0db40afb7a7d33eb4e45dbbd5fe265c15.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

To remove files, we can use the ‘rm’ command, with the name of the file to remove:

<figure data-orig-width="652" data-orig-height="515" class="tmblr-full"><img src="https://64.media.tumblr.com/6ba65bb9279d3f8997b81bf92e510e4d/4f4f6e4f74f0ec87-14/s540x810/e9469810b79947e768f451564b930fc6a2295479.png" alt="image" data-orig-width="652" data-orig-height="515"/></figure>

To create directories, we use the ‘mkdir [directory name]’ command, and we can use rm with the ‘-rf’ flag to remove empty directories.

You have now learned the beginning of how to navigate around directories and files with a Linux terminal. There is a lot more but that can be learned over time. This was just a quick crash course. I would advise you play around the terminal and learn for yourself. The terminal may look imposing but it is essentially just what you would do on the user interface.

<a href="https://ubuntu.com/tutorials/command-line-for-beginners#1-overview">Ubuntu has a good tutorial on how to use the terminal</a>
