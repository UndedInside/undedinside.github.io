---
layout: page
title: 'Staying Safe Online pt. 4: Proxies and VPNs'
date: '2021-02-02T09:49:19+00:00'
tags:
- Staying Safe Online
- hacking
- hacking guide
- hacking tutorials
- internet
- technology
- tech
- internet safety
- tech guides
- technology guide
- vpn
- proxy
tumblr_url: https://undedinside.tumblr.com/post/642019344393584641/staying-safe-online-pt-4-proxies-and-vpns
---
When discussing privacy online a common suggestion is to use a VPN or a proxy with the assertion that it will protect your privacy, but if you are like me you may not know how either works or even that there is a difference between the two. In this post I will teach you what they are, and how they are different to each other.

## What is a Proxy?

You can think of a proxy as a ‘go-between’ that sits between your machine and the server you want to connect to (I’m going to use a webserver for this example, but it could be anything). When you want to interact with the website, you send the requests through the proxy server which sends them to the website. The proxy server then receives the result from the webserver and sends it back to you.  This hides your IP address, as the webserver only sees the IP address of the proxy server, not of your machine.

<figure data-orig-width="601" data-orig-height="61" class="tmblr-full"><img src="https://64.media.tumblr.com/afe3515e233e1114c6c4c038a7a32b7d/20eb1ff2991cdfbb-52/s540x810/055ac127a0ecf086ed80f30575f4e270e3bab9a8.png" data-orig-width="601" data-orig-height="61"/></figure>

## How is a VPN Different to a Proxy?

A VPN is also a ‘go-between’, but this time the data you send between the VPN and the proxy is encrypted (data sent between the VPN server and the webserver are not necessarily encrypted). A VPN also hides your IP address, as well as hiding your browsing from people on the same network using packet sniffers, which a proxy does not.

<figure data-orig-width="601" data-orig-height="61" class="tmblr-full"><img src="https://64.media.tumblr.com/c548c8a1e097c5c04bb424844cf6060a/20eb1ff2991cdfbb-12/s540x810/6f9ae16f54e8c7513639680fab9da34bf6da3c38.png" data-orig-width="601" data-orig-height="61"/></figure>
