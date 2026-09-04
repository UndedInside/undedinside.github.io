---
layout: page
title: Finding Open Ports with Nmap
date: '2020-08-20T12:01:17+00:00'
tags:
- hacking
- pentesting
- linux
- linux tutorial
- guide
- hacking tutorials
- nmap
tumblr_url: https://undedinside.tumblr.com/post/626984776053735424/finding-open-ports-with-nmap
---

When traffic is sent to a computer, it is sent to a certain port. This port depends on the software sending/receiving the traffic. This ensures that the data is sent to the software that needs it, for example websites normally operate on port 80 or 443 (depending on if the site uses HTTP or HTTPS respectively), whereas SSH uses port 22. You can read more on ports [here]("https://en.wikipedia.org/wiki/Port_%28computer_networking%29").

Nmap is a tool which allows hackers or network administrators to tell which ports are open on a device. This information can be used to find vulnerable services to exploit, or to find services which shouldn’t be running and which a hacker or malware may have added.

The official site for nmap is [here]("https://nmap.org/"), and it can be downloaded from there, however it comes packaged with Kali. I will be scanning a VM running [metasploitable]("https://docs.rapid7.com/metasploit/metasploitable-2/"), which is an OS created by the creators of metasploit (a hacking tool, but more on that another day) and is intentionally vulnerable. I will be using this machine in many of my tutorials to demonstrate techniques/attacks. Creating a Metasploitable VM is identical to creating a Kali box, but using a Metasploitable image instead.

After booting up the Metasploitable machine, we see something like this:

<figure data-orig-width="722" data-orig-height="465" class="tmblr-full"><img src="https://64.media.tumblr.com/e0da0ed81fb2e507c66e7bb9715baa27/7c0f899f31a8df6c-ea/s540x810/897e968b44df3d49f0023d8a35074396ee6a7392.png" alt="image" data-orig-width="722" data-orig-height="465"/>

We can then run the command ‘ip route’ to find our local IP address.

<figure data-orig-width="722" data-orig-height="465" class="tmblr-full"><img src="https://64.media.tumblr.com/2ababef208cfe56e43aeaaa24edf9f62/7c0f899f31a8df6c-a6/s540x810/72e78a3d128983b91bf2c90fee327747ea5d738a.png" alt="image" data-orig-width="722" data-orig-height="465"/>

Quite a lot is shown, but what we are looking for is the address after ‘src’. This tells me that my local IP address is 192.168.0.90.

Without closing Metasploitable, we open our Kali VM as well and log in. to check that we can connect to Metasploitable, we will ping the address we just found.

<figure data-orig-width="650" data-orig-height="513" class="tmblr-full"><img src="https://64.media.tumblr.com/fd05a83cfda8b935d9de3e043b92fa7b/7c0f899f31a8df6c-46/s540x810/3ab748d216c50b2c86a872621628bcf73e107fa2.png" alt="image" data-orig-width="650" data-orig-height="513"/></figure>

‘64 bytes from 192.168.0.90′ tells me that I am getting a response from Metasploitable. Let’s start an nmap scan.

We are going to start with just a simple scan. I will type ‘nmap 192.168.0.90′ without any other flags.

<figure data-orig-width="1280" data-orig-height="720" class="tmblr-full"><img src="https://64.media.tumblr.com/b2e3d063e474b012ce0a017900361525/7c0f899f31a8df6c-cd/s540x810/e55ef60eeb544540acec00c96d514e14515acaf3.png" alt="image" data-orig-width="1280" data-orig-height="720"/></figure>

Here we can see that there are 21 ports running. Knowing what ports are open is useful, but we can find more information. Let’s find the OS with the -O flag (bear in mind that this requires sudo)

<figure data-orig-width="1280" data-orig-height="720" class="tmblr-full"><img src="https://64.media.tumblr.com/e3eb6572181597375e7d121c6c75eecf/7c0f899f31a8df6c-eb/s540x810/ce1c81aff6487643838ad638a2e78676aa12692a.png" alt="image" data-orig-width="1280" data-orig-height="720"/></figure>

Along with the same information from before, we now have more information. We now know the MAC address, the OS it is running (Linux 2.6), and some more information about the OS.

Nmap can also tell us (a guess) about the software running on each port with the -sV argument.

<figure data-orig-width="1280" data-orig-height="720" class="tmblr-full"><img src="https://64.media.tumblr.com/d51e84e29a2b62ae4bba0be27e8daab8/7c0f899f31a8df6c-06/s540x810/ced29780be1d563672dd6bc664b74c1452368f1a.png" alt="image" data-orig-width="1280" data-orig-height="720"/></figure>

We can use this software version to search for exploits, and I will write another guide on that soon but here is a quick example of just some of the exploits.

<figure data-orig-width="1280" data-orig-height="720" class="tmblr-full"><img src="https://64.media.tumblr.com/024fae89c89f8bb619d5ec4fd4260c44/7c0f899f31a8df6c-5f/s540x810/0f09c308090643bf8ce64c313f03d49cb149276c.png" alt="image" data-orig-width="1280" data-orig-height="720"/></figure>

Using the -h flag with nmap will output all of the available options:

<figure data-orig-width="1280" data-orig-height="720" class="tmblr-full"><img src="https://64.media.tumblr.com/04d9c0fe5fc055f7c1f9f03f074ac4b0/7c0f899f31a8df6c-33/s540x810/aa6e29ab1d88dfa30e83aa11acc06090a5e5f3e2.png" alt="image" data-orig-width="1280" data-orig-height="720"/></figure>

As you can see, there are a lot of options. I recommend using a site like [HackTheBox]("https://www.hackthebox.eu/") or [TryHackMe]("https://tryhackme.com/") to give you a place to practice (I have found TryHackMe is better for beginners), or you can practice with a Metasploitable box.

Nmap is a very useful tool and enables you to find so much information. It is worth learning well and I haven’t begun to scratch the surface of all the functionality.
