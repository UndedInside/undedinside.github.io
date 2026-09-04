---
layout: post
title: Using TryHackMe
date: '2021-01-02T17:32:36+00:00'
tags:
- hacking
- hacking tutorials
- hacking guide
- linux
- linux tutorial
- linux terminal
- linux guides
- Kali
- kali linux
tumblr_url: https://undedinside.tumblr.com/post/639239985420271616/using-tryhackme
---
If you’ve been reading my blog, you may have noticed me mention the site TryHackMe (In my post on [nmap](/tutorials/hacking-pt-1-finding-open-ports-with-nmap) for example). I use this site often, and in my experience it has been a brilliant resource in learning not only hacking, but also using the Linux terminal and other more broad subjects. In this post I will teach how to make an account, connect to the TryHackMe network, and start hacking.

## Creating an Account:

The first step is to create an account at <a href="https://tryhackme.com/signup">tryhackme.com/signup</a>. Here you can choose a username, an an experience level to describe your level of experience with hacking (This isn’t displayed, so don’t feel bad if your experience level is low)

<figure data-orig-width="1658" data-orig-height="905" class="tmblr-full"><img src="https://64.media.tumblr.com/44de983597577e7970f90aa6a804425e/68f2ccab45e3457b-88/s540x810/fbeb67a0f5dc53b1106a0c743d8ecb2cf9815b5e.png" alt="image" data-orig-width="1658" data-orig-height="905"/></figure>

After signing up, you’ll be taken to a ‘room’. Rooms are a series of activities to help you learn an aspect of cyber security. Each task has at least one ‘question’ (although there don’t always require an answer, sometime you just need to read or do something). This is what the room looks like for me, but I think it’s different depending on your experience level:

<figure data-orig-width="1920" data-orig-height="922" class="tmblr-full"><img src="https://64.media.tumblr.com/25cae80195a2009230d6edbaeb619856/68f2ccab45e3457b-55/s540x810/959c91a0727e5abe09ae8fbce7f2491c07d3d8cb.png" alt="image" data-orig-width="1920" data-orig-height="922"/></figure>

On completing all the tasks of a room, you will be congratulated. You can use this to share your achievement on social media, or just click the cross if you want to keep your success to yourself.

<figure data-orig-width="1277" data-orig-height="837" class="tmblr-full"><img src="https://64.media.tumblr.com/a07ebc042eb365830a4fc7199b7c8b91/68f2ccab45e3457b-83/s540x810/ce0d4c8fae7d985fbae6ec4580190a77fdcf4f6f.png" alt="image" data-orig-width="1277" data-orig-height="837"/></figure>

You can now go to the Dashboard. This is the home screen, from which you can navigate the website as well as see statistics on your learning. I’m going to let you discover most of what the website has to offer, but I’ll walk you through a few things.

<figure data-orig-width="1908" data-orig-height="923" class="tmblr-full"><img src="https://64.media.tumblr.com/c5d201929e65efab6b847e88482a8d71/68f2ccab45e3457b-79/s540x810/9d39d07912b051b65398418294d7337f3f557acd.png" alt="image" data-orig-width="1908" data-orig-height="923"/></figure>

‘Pathways’ are groups of rooms with a similar subject, designed as more structured learning than doing the rooms on their own. Some of these rooms require a paid VIP account, but all pathways have at least one free room for you to do. A ‘series’ is a similar thing, but giving fun challenges to test your knowledge. These two groups don’t come close to including everything TryHackMe has to offer, for that there are individual rooms you can access from the ‘Learn’ tab

If you feel like giving yourself an extra challenge try the ‘Compete’ tab to either check the leaderboard and see where you place, or compete against other hackers in a King of the Hill.

Before you get into doing activities however, there’s one important thing to know. Many rooms include a virtual machine to hack against, but in order to connect to it you have to connect to the TryHackMe VPN (Virtual Private Network). I’ll explain what a VPN is in a later guide, but for now just know that it connects you to TryHackMe’s network, which has the VMs to hack on it.

## Connecting to the VPN:

To connect to the VPN, the first thing you need to do is download the configuration file. this can be done by clicking your profile in the top right, then ‘connect’, or by going to tryhackme.com/access. A download will start for a [your username].ovpn file - click ‘Save File’ and the download should be finished very quickly.

Open a terminal and cd to your Downloads directory. You should see your .ovpn file there.

<figure data-orig-width="911" data-orig-height="558" class="tmblr-full"><img src="https://64.media.tumblr.com/7b4e58e4bc22386244e21ea7af18b2f6/68f2ccab45e3457b-96/s540x810/f8cc50d3a4086d56ff32108e6a71da6963235e4f.png" alt="image" data-orig-width="911" data-orig-height="558"/></figure>

You should have openVPN installed by default on Kali, so you simply start the VPN connection with the command “sudo openvpn [username].ovpn”, after running the command you should see a lot of output. You can now open a new terminal window or tab with CTRL+SHIFT+T, and get to hacking.

<figure data-orig-width="1126" data-orig-height="798" class="tmblr-full"><img src="https://64.media.tumblr.com/4d30a871930c12073bc5dc3f5d31e08f/68f2ccab45e3457b-fe/s540x810/6a24cd7b08813511a75e56030764fcf2b6278c1c.png" alt="image" data-orig-width="1126" data-orig-height="798"/></figure>

(I had to switch machines and TryHackMe accounts because I had an error. If you have problems connecting, please send me a <a href="https://twitter.com/UndedInside">DM on twitter</a>

You can then check  you are connected, by going back to the ‘access’ page. You should see this:

<figure data-orig-width="591" data-orig-height="284" class="tmblr-full"><img src="https://64.media.tumblr.com/33945f619b9148e9cf34864d47677349/68f2ccab45e3457b-5e/s540x810/b581dd847118bde78e1d26a5ae26815705718442.png" alt="image" data-orig-width="591" data-orig-height="284"/></figure>

This panel also tells you your Internal IP address, which is useful for executing some exploits/shells, in case you forgot [how to find that from the terminal](/tutorials/linux-pt-2-basic-networking-commands). Your VPN server name may differ, depending on your geographic region.

## Conclusion:

Go forth and hack things! As I mentioned before, TryHackMe is a great resource for hands-on learning. There are rooms about all manner of things, from cyber security to python programming and general Linux use.

(Btw on the dashboard, there is a friends search bar. Feel free to add me as a friend if you want, I’m still UndedInside with the same picture).
