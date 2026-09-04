---
layout: page
title: "Binary pt. 1: Converting Decimal to Binary and Vice Versa"
date: 2020-11-28T17:05:32+00:00
tags:
- binary
- binary tutorial
- tutorial
- programming tutorial
- programming
tumblr_url: https://undedinside.tumblr.com/post/636067389526720512/binary-pt-1-converting-decimal-to-binary-and
category: post
---
# Decimal to Binary:

Binary seems intimidating, I know. It’s just so _different_ to what we’re used to. Luckily though it’s not actually that hard, so in this tutorial I will teach you how to convert decimal to binary, and my next guide will be the other way around.

The first thing to know is that a single binary digit is called a “bit”, and they are normally grouped in eights, called “bytes”. An example of a byte is “01000101“. There are 256 combinations of bits from one byte, so the biggest number that can be stored is 255 (one of the combinations is zero).

Let’s move on to how to convert a number from decimal to binary. I’m going to get a random number from google that we can work out together.

<figure data-orig-width="732" data-orig-height="449" class="tmblr-full"><img src="https://64.media.tumblr.com/954a6de631db5131df325a3d0baebc81/509edb90f654dada-2b/s540x810/2c72229878884409ac4d0e809bedf2c4c1c206b4.png" alt="image" data-orig-width="732" data-orig-height="449"/></figure>

176, thank you google.

I start by writing out what each bit is worth if it is 1 as headings in a table. Counting from the right, each bit is worth double the last one, counting from 1. This gives me the following table:

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/408a48e6ca011bc052496521e58e3a26/509edb90f654dada-41/s540x810/39ab5a81955078ff9fbfc8f9a2822807cece24db.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

Now we start reading from the left. If the heading we are on can be subtracted from the number we are trying to convert and give a result above 0, we put a one in that heading, otherwise we put a 0.

That is very wordy so I’ll show you instead. 176 - 128 = 48, so we put a 1 there:

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/cc8217e353b9240d41823ea4f11fdb6e/509edb90f654dada-8f/s540x810/b08dbd258cf49b3ade7e606188b8afc4176d72a8.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

After the last calculation we are left with 48. 48 - 64 = -16, so we put a 0 in that column.

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/d166396f7483431582f3d82ae96c42e4/509edb90f654dada-88/s540x810/3c9dec19e4f1c8aadcdab42bbae0fa9ae0c0c9b4.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

We still have 48. 48 - 32 = 16.

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/ec390ddb8db86f5d69a773a8689a4613/509edb90f654dada-90/s540x810/9c1f28265956317f2aa9b40c93c75687d3176c57.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

16 - 16 = 0, so we put a 1. We are left with nothing, so we know the rest of the bits are going to be 0.

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/6e8fa326076ba1748910d0b299f3d50d/509edb90f654dada-45/s540x810/22f04e64f997afdf133742ee2c37662049124756.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

Our byte is 10110000.

# And Vice Versa:

So know you know how to convert to binary, but how do you convert from binary to decimal? The short answer is you do the opposite.

For this we’re going to use the same byte we just worked out (10110000). Write out our byte, then write the headings on top.

<figure data-orig-width="241" data-orig-height="41"><img src="https://64.media.tumblr.com/6e8fa326076ba1748910d0b299f3d50d/509edb90f654dada-45/s540x810/22f04e64f997afdf133742ee2c37662049124756.png" alt="image" data-orig-width="241" data-orig-height="41"/></figure>

Now we add all of the headings of ‘on’ bits together. We work out 128 + 32 + 16 which gives us an answer of 176.

## Practice:

I cannot stress enough how useful practice is for learning this, so here are some practice questions. Once you’ve finished you can look up the answers online to check.

1. 129 to binary
2. 10100010 to decimal
3. 255 to binary
4. 254 to binary
5. 00100011 to decimal

If you have any questions feel free to contact me and ask and I’ll help as much as I can.
