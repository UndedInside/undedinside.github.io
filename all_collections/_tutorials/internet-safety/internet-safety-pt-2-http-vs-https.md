---
layout: page
title: 'Staying Safe Online pt. 2: HTTP vs HTTPS'
date: '2021-01-19T18:10:04+00:00'
tags:
- internet
- internet safety
- staying safe online
- tutorial
- guide
- technology
- tech
- tech guides
tumblr_url: https://undedinside.tumblr.com/post/640782491172601856/staying-safe-online-pt-2-http-vs-https
---
You’ve probably noticed the padlock symbol in your address bar, which means that your browsing is safe but do you know the extent of that safety? To be precise, that padlock means that the page is being served using HTTPS.

## What is HTTP?

Before discussing HTTPS, we need to go over HTTP first.

Data is sent over the World Wide Web (note: the World Wide Web is a part of the internet, but is not the internet) using the protocol HTTP. HTTP Stands for Hypertext Transfer Protocol, and it dictates how the _client_ (in this case, your browser) sends and receives data from the server.

This data is sent in cleartext over the internet, meaning that anyone on the same local network can ‘sniff’ your data using software like wireshark, allowing them to see what sites you are visiting. HTTP also doesn’t verify the site that you are browsing is the actual site, making HTTP vulnerable to something called a Man- or Meddler-in-the-Middle (MitM) attack. This is when an attacker pretends to be the web-server and can then intercept your browsing by routing all of your HTTP traffic through them.

To remedy these problems HTTP was improved with a protocol called HTTPS, which is a more secure version of the older protocol.

## What is HTTPS?

HTTPS is a complicated thing, so for now we’re not going to go over how it works. For now it is important to know that it does two main things that HTTP doesn’t:

For a start, it verifies that the web-server is actually who it says it is. This protects you against MitM attacks: This is where a cyber-criminal impersonates a legitimate website, and routes all of your traffic with that website through them. This allows them to see and possibly edit data sent.

<figure data-orig-width="401" data-orig-height="192" class="tmblr-full"><img src="https://64.media.tumblr.com/6b4cdf67bd233a32f09a78adeb06e7fb/852a019b79da9a68-3d/s540x810/bb0ef97996b9fb313a3fa0a11258f8be063d109e.png" alt="image" data-orig-width="401" data-orig-height="192"/></figure>

HTTPS also encrypts data sent over the internet. This protects you against hackers using tools like <a href="https://www.wireshark.org/">wireshark</a> and <a href="http://aircrack-ng.org/">aircrack-ng</a> to ‘grab’ packets sent over WiFi.

## What Doesn’t HTTPS Protect Against?

There’s an important distinction to be made when I say that HTTPS verifies that the server says it is who it says it is. If a site wants to use HTTPS, they need a certificate. HTTPS ensures that the certificate belongs to the server, but it does not make sure the server is the one you think it might be.

A malicious actor could create a website called “amazin.com” for phishing purposes, and then get a certificate to enable HTTPS. This would make https://amazin.com secure, _but it would not be safe._ Trying to buy anything on that site would lead to your credit card details being sent to the attacker. As my little brother put it: “It may protect you against a Meddler in the Middle, but doesn’t help if the website you’re on is the Meddler”.

## Conclusion:

HTTPS doesn’t ensure that the website is safe, only that the connection between you and the website is private. A lack of HTTPS also doesn’t mean the website you are on is unsafe, but you should exercise caution if what you are doing on the non-HTTPS is sensitive.
