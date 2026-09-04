---
layout: page
title: Hacking Metasploitable
date: '2020-08-23T12:01:29+00:00'
tags:
- hacking
- hacking guide
- hacking tutorials
- linux
- linux tutorial
- kali
- pentesting
tumblr_url: https://undedinside.tumblr.com/post/627256579820060672/hacking-metasploitable
---
It’s time to put all our skills to the test. In this guide we are going to scan a computer, find an exploit, and use it to gain access to the machine. The first step is to start a metasploitable VM, and get the IP address.

<figure class="tmblr-full" data-orig-height="400" data-orig-width="720"><img src="https://64.media.tumblr.com/c46140dca2162d3d5e0486530f8396fa/a83b84a3cd593f83-61/s540x810/f74c4a442b9650ed970aad9cbfe315a97bc127d5.png" data-orig-height="400" data-orig-width="720"/></figure>

I can see that my target’s IP is 192.168.0.90, so now I’m going to run an nmap scan with the -sV flag to find out what software is running. This gives the following results:

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/928b8bbe89e5e3cb262601fe5e049cd4/a83b84a3cd593f83-04/s540x810/8979f8072e38416c4dc13db395d45b0864d0759d.png" data-orig-height="1024" data-orig-width="1858"/></figure>

I’ve used vsftpd as an example in my previous guides, and since it is first on the list I’m going to try hacking Metasploitable through this. The first step is to fire up metasploit and search for exploits.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/1c9fbd18445a5be423812f02c607b100/a83b84a3cd593f83-b5/s540x810/71229c15db1270d1af6784071f7e9084987980d8.png" data-orig-height="1024" data-orig-width="1858"/></figure>

There aren’t many exploits for it, but there is a backdoor which I can try to use. using the command ‘show options’ will show me what I need to set.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/55280120e5f1e1acf368b6375bc010ee/a83b84a3cd593f83-1c/s540x810/aee6fcb695c58ffd7fb6db824052c87966ba584e.png" data-orig-height="1024" data-orig-width="1858"/></figure>

I now know I need to provide RHOSTS, which is defined by ‘The target host(s)’. I’m only attacking one target, so I set RHOSTS as the target IP.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/f7c0fde8d58281c7f47692a91a204a1f/a83b84a3cd593f83-e3/s540x810/3732d4e751be5061778a9d78f6bfb1ae29d40c23.png" data-orig-height="1024" data-orig-width="1858"/></figure>

Using the command ‘exploit’ should now give me access to the Metasploitable machine.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/e9e225e4d89540e839e781b7dd72418b/a83b84a3cd593f83-fb/s540x810/06fb5dc47a8c382d9517316c0395d3fa02fc6c82.png" data-orig-height="1024" data-orig-width="1858"/></figure>

Success! This exploit doesn’t give us a shell, but we can type linux commands in.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/fde27f6adfb25b58fdaa9009712f6f3c/a83b84a3cd593f83-d8/s540x810/426c899d21ebb250d4040ef285097f5a9467d380.png" data-orig-height="1024" data-orig-width="1858"/></figure>

It’s hard to see, but I have used the ‘ls’ and ‘pwd’ command to demonstrate that I have access. I have demonstrated this further by navigating to msfadmin’s home directory and viewing one of the files.

<figure class="tmblr-full" data-orig-height="1024" data-orig-width="1858"><img src="https://64.media.tumblr.com/3dea7af3ea7d35fc1b1ed1387770a744/a83b84a3cd593f83-d5/s540x810/55387b64bf4e98ecdb5a1e6ac7973639e9f18be8.png" data-orig-height="1024" data-orig-width="1858"/></figure>

If you’ve followed this walkthrough you should also have gained access and hacked your first machine. If you haven’t you can send me a message or an ask and I can try to help you.
