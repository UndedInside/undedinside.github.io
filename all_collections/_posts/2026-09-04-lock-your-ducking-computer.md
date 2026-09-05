---
layout: post
title: "Lock Your Ducking Computer!"
date: 2026-09-04 21:14:00 +0000
categories: blog
hook: "Adventures in DuckyScript"
---
I knew I wanted to be a hacker since I first laid my eyes on [hak5.](https://hak5.org) Specifically it was the WiFi Pineapple that stole my heart but, as a broke teen, the only thing I could afford was the Rubber Ducky.

I had no idea what I was doing. Beyond a simple phone brute-forcer, I can't say I did anything with it. But I was carrying a hacking tool around with me at all times. It looked like a normal USB but it could type at thousands of words a minute! All I had to do was learn a little more and then no one was safe. I was ~~a scriptkiddie~~ a hacker!

Unfortunately I never learned that one extra piece of information that would make me dangerous. The Ducky stayed in my bag never to pwn.

All this changed, however, when I bought the [Flipper Zero](https://flipper.net) and spotted a familiar option in the menu. 'BadUSB'. Just like a Ducky.

I had learned a little bit more since my teen years with the unused Ducky. I knew what both a bind **and** reverse shell were. I was aware of some tips and tricks, and had been going to conferences for a couple of years. Whats more, the Flipper Zero used DuckyScript! The very same scripting language I had fumbled around with! This time, when I sat down to write some hacks, I knew what I was doing.

You can find the fruits of this labour (and development) [here on my GitHub.](https://github.com/UndedInside/DuckyScriptPayloads)

I'll still be honest, there's nothing particularly ground-breaking there, but when writing scripts I tried to keep a particular scenario in mind:
- I'm on a pentest job.
- Someone has stepped away from their computer and left it unlocked.
- I don't know how long of a window I've got, but I want to make every second count.

To this aim I have tried to come up with scripts that will utilize the Ducky/Flipper's rapid typing speed and make the most of the situation. Maybe I'll disable Windows Defender, then plant a bind shell to connect to it later. Maybe I'll set up persistant access on this Linux/Mac machine. Maybe I'll just rick roll them instead, as a friendly reminder to...

**Lock Your Ducking Computer!**
