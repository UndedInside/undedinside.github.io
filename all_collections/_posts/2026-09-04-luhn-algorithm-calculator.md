---
layout: post
title: "Luhn Algorithm Calculator"
date: 2026-09-04 18:35:00 +0000
categories: blog
---
(This project was originally completed 2021-09-19)

I was buying something online, when I noticed it was telling me I had mistyped my card details before I had pressed submit. It was telling me I had made a mistake _in real time!_ In my head, there were two options:
1. The site knows my card details before I even enter them or,
2. It can somehow work out what they are meant to be.

Out of fear of psychic identity thieves, I decided to do some googling and found out the website was using something called [_Luhn Algorithm._](https://en.wikipedia.org/wiki/Luhn_algorithm)

The Luhn algorithm is a simple 'check digit'[^1] algorithm which is used in a number of different contexts - including credit card numbers. The way it works is the bank only 'comes up' with the first 15 digits of the card number, with the last one worked out by the Luhn algorithm. You can then validate a card number by removing the last digit, calculating what it should be with the first 15, then comparing it to the last one you were provided. If they match then the number is valid, if they don't then they probably typed the number in wrong. The Luhn algorithm doesn't tell you if a card is in use - only that the number is a valid one.

Not only did I find this information about the Luhn algorithm but I also found the psuedocode for it. I had been looking for an excuse to practice my C++ so I took this as an opportunity.

## How the Luhn Algorithm Works:
The steps to calculate a check digit are:
1. From the left, double every second digit
2. From the right, subtract 9 from the digit if the digit is more than 9
3. Sum all the resulting digits
4. Calculate (10 - (<answer from 3> mod 10)) mod 10[^2]
5. The number you get from that is your checkbit.

Taking the number 79927398713 as an example, we can calculate it by first removing the 3 and then:

| Digits (reversed) | 1 | 7 | 8  | 9 | 3 | 7 | 2 | 9 | 9  | 7 |
| :---------------- |:-:|:-:|:--:|:-:|:-:|:-:|:-:|:-:|:--:|:-:|
| Multipliers       | 2 | 1 | 2  | 1 | 2 | 1 | 2 | 1 | 2  | 1 |
|                   | = | = | =  | = | = | = | = | = | =  | = |
|                   | 2 | 7 | 16 | 9 | 6 | 7 | 4 | 9 | 18 | 7 |
| Sum digits        | 2 | 7 | 7  | 9 | 6 | 7 | 4 | 9 | 9  | 7 |

The sum of all these digits is 67.

67 mod 10 is 7

10 minus 7 is 3

The check digit we calculated was 3, as was the one we were given, so we can verify that this is correct.

## My Implementation:

You can find my implementation of a Luhn algorithm calculator [on my GitHub](https://github.com/UndedInside/ULC)

Use the `-c` flag to calculate a check digit, or the `-v` flag to verify a full number (This will return `1` if valid and `0` if invalid)

[^1]: Cambridge dictionary: "noun, a number that is used in a computer program to help find or prevent errors" not to be comfused with a Czech digit, which is what people of Czechia have on the end of their hands
[^2]: The reason for this last mod 10 is that, without it, if the sum from step 3 is a multiple of 10, the final answer for the check digit would be 10 and not 0. 10 is obviously not a digit, so a valid number would be marked as invalid because it has a 0 at the end and not the impossible 10. Thank you to my friend Blake for finding out the reason for that. I have had to patch the code almost 5 years later.
