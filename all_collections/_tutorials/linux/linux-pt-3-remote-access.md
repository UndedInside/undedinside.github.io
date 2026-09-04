---
layout: page
title: 'Linux pt. 3: Remote Access'
date: '2020-12-23T12:01:42+00:00'
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
tumblr_url: https://undedinside.tumblr.com/post/638313197870415872/linux-pt-3-remote-access
---
Sometimes you need to do work on a computer, but won’t be able to do it physically. Linux has commands to enable you to use the terminal of another device across the internet. The preferred method of doing this is with a protocol called SSH.

## Using SSH:

To SSH into a device, you need two pieces of information: the IP of the server, and a username on the server to log in as. I’m going to be connecting to my metasploitable VM, so I know the username is ‘msfadmin’ and I can find out the IP. I can then start to connect with the command ‘ssh [username]@[IP]'

<figure data-orig-width="911" data-orig-height="558" class="tmblr-full"><img src="https://64.media.tumblr.com/a041e42f3dbe05edb7d9cc3f45e09423/d7144c3f918f452e-8a/s540x810/91d7672145e319911320770c2dadecfe32677621.png" alt="image" data-orig-width="911" data-orig-height="558"/></figure>

When you first connect to a server, you’ll be greeted with something looking like this. This can be used to help you authenticate that the server you’re connecting to is the one you’re intending to, but for now you can just type ‘yes’ to connect

<figure data-orig-width="913" data-orig-height="560" class="tmblr-full"><img src="https://64.media.tumblr.com/6c410c56b7a7ad77c7b1550ebd28f430/d7144c3f918f452e-4b/s540x810/0bcf9e288683820933020e2bdca96bbab264f0d8.png" alt="image" data-orig-width="913" data-orig-height="560"/></figure>

After entering ‘yes’, you should be greeted with a login prompt, where you can enter your password (’msfadmin’ in this case) to log into the server and be given a prompt. In this example I think I took too long and the connection closed, but just restarting the connection worked.

You can now run commands as you would on your local machine:

<figure data-orig-width="913" data-orig-height="560" class="tmblr-full"><img src="https://64.media.tumblr.com/4d535a0b84a3a233d60ff521e47b3a40/d7144c3f918f452e-5f/s540x810/b0018898eb49e244524101824c10d19d8a8a8568.png" alt="image" data-orig-width="913" data-orig-height="560"/></figure>

## Using SSH Instead of Telnet:

The SSH protocol isn’t unique in what it can do, the telnet protocol does a similar thing and was used much before SSH was created. One main problem with telnet is the fact that data sent over it is unencrypted. This means that hackers can intercept the data and read it, potentially giving them passwords and sensitive information.
