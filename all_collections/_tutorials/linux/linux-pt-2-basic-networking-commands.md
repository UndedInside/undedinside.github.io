---
layout: post
title: 'Linux pt. 2: Basic Networking Commands'
date: '2020-12-21T17:00:55+00:00'
tags:
- linux
- linux tutorial
- linux terminal
- linux guides
- linux terminal guide
- Kali
- guide
- hacking guide
tumblr_url: https://undedinside.tumblr.com/post/638150829091799040/linux-pt-2-basic-networking-commands
---
## Ping:

Ping is the networking command I use most often. It is used to test if you can reach a device, and if so how quick the connection is. To use this command, you type the word ‘ping’ followed by either a domain (google.com) or an IP address.

<figure data-orig-width="911" data-orig-height="558" class="tmblr-full"><img src="https://64.media.tumblr.com/d0862e4ab73074562046907b71697c0d/2985e6475aa222b9-69/s540x810/91f2a16d310bead0cc662a0ea2aed9f08f96a429.png" alt="image" data-orig-width="911" data-orig-height="558"/></figure>

Ping sends a stream of packets to the location you give it, and waits for a response. After running the command, we can see the response (64 bytes from&hellip;), and on the end of the line is the time it has taken to get that response in milliseconds. The ping command will run indefinitely, so to end it you use the keyboard shortcut CTRL+C. You can then get some statistics about the connection. If you don’t have a connection to the device you’re pinging, you will see something like this:

<figure data-orig-width="911" data-orig-height="558" class="tmblr-full"><img src="https://64.media.tumblr.com/7512cdea55e4d09d4cdac725ce3f9563/2985e6475aa222b9-2f/s540x810/af807a7893a559f64e298b0fee2302cb981539fd.png" alt="image" data-orig-width="911" data-orig-height="558"/></figure>

Note that ping can also be used to give you an IP address of a domain. After pinging a domain, it will give an IP address. Here I find an IPv6 address after pinging bing.com:

<figure class="tmblr-full" data-orig-height="558" data-orig-width="911"><img src="https://64.media.tumblr.com/02e5918d06c14a0e16e80605cf4146c4/2985e6475aa222b9-ee/s540x810/830ec973988e3b331fcf7b508a07dfac3700abb8.png" data-orig-height="558" data-orig-width="911"/></figure>

## ip address:

This command tells you your local IP address. There’s a lot of information that may not be useful to you however.

(I used my own Kali machine for this, because my tutorial one has too many IPs and the output was cluttered)

<figure data-orig-width="1079" data-orig-height="905" class="tmblr-full"><img src="https://64.media.tumblr.com/3a2deb991f581df2b028ab4dbfceb974/2985e6475aa222b9-e2/s540x810/ba73be6beea35ed455524cfe78f6a6a158d8f5c5.png" alt="image" data-orig-width="1079" data-orig-height="905"/></figure>

For a start, we can ignore everything in section 1. This is the _loopback interface_ and while it can be useful for diagnosing connection problems, it doesn’t tell us our IP: for that we need to look at section 2. Your internal IP address is listed under inet (in this case it’s 192.168.129.132), with your IPv6 address listed under inet6.

That is a lot of information to take in, but all you really need to know is that your IP address on your current network is found next to ‘inet’.

## Conclusion:

I know this is a very short guide, but these are the two non-hacking networking commands I use most often; they are fundamental and it’s always important to have a solid knowledge of the foundations.
