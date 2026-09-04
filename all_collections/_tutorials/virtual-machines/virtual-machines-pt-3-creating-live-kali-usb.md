---
layout: post
title: Creating Kali Live USB
date: '2021-01-14T06:25:58+00:00'
tags:
- linux
- linux tutorial
- Kali
- Kali Linux
- linux guides
- hacking
- hacking tutorials
- hacking guide
tumblr_url: https://undedinside.tumblr.com/post/640285208468406272/in-the-past-i-have-written-guides-on-how-to-set
---
In the past, I have written guides on how to set up VMs (Virtual Machines) using both [VMWare](/tutorials/virtual-machines-pt-1-kali-vmware.html) and [VirtualBox](/tutorials/virtual-machines-pt-2-kali-virtualbox.html) programs, but what if you’re looking to take your hacking on the go? For this you need something more portable. VirtualBox does have the ability to be <a href="https://t.umblr.com/redirect?z=https%3A%2F%2Fwww.howtogeek.com%2F188142%2Fuse-portable-virtualbox-to-take-virtual-machines-with-you-everywhere%2F&amp;t=NGQ5NjUzYTBjM2YxZTg1YjcwN2E2Y2MwNmIwMDM0NTM3YzAxOGY5MyxhMDg0YmQ0OTUyMWJjNmE5Y2FmYzhiMmQxMjJkOGRkYmQ0MGUyNDdk&amp;ts=1610662912">installed on a thumb-drive or external hard drive</a>, but another way you can achieve this is with a bootable USB.

## What is a Live USB?

An operating system can be placed onto a thumb-drive, and it can then temporarily replace the PCs operating system. This can have a variety of uses: from being used to help diagnose problems and fixing the computer, to just taking OS’s for a ‘test drive’.

The drive is inserted into the computer while it is turned off, and then when it is turned on, it boots from the USB instead, allowing you to use the OS on the drive.

## How to Create a Live USB?

To create a live USB, you need three things:
1. A USB stick (at least 4GB)
2. Rufus (download from <a href="https://t.umblr.com/redirect?z=https%3A%2F%2Frufus.ie%2F&amp;t=MjIxOTUzZTgzMzcxNDE5ZmViYTIwMTAxZjNlZDJiYjE3ZTk3ZjZkMiw0MjNmYjNiYjE3NGJhOTlkY2JhN2Y3OTUxZjFhZTQyNjA2YWMzMmM4&amp;ts=1610662912">here</a>)
3. Kali live iso (download from <a href="https://t.umblr.com/redirect?z=https%3A%2F%2Fwww.kali.org%2Fdownloads%2F&amp;t=NzAxNWYxNzRlMzk2YmEwY2NiNDVkNTk3NjZkZTk5NDVjY2M1YmZhYiw2YmExZGQ4M2RhMzA3YTJmNDVmYTM4NTllMWJjMDgwYTEzMWJjYmZj&amp;ts=1610662912">here</a>. Make sure you download the live version)

The Rufus download shouldn’t take so long, but the iso file will take some time to download. Sit back, and relax. Maybe read a little, or watch a movie, This tutorial can wait.

Finished? Good.

After downloading the iso, you can check the hash of the file against the hash against the website to confirm that the file hasn’t been corrupted. There are a variety of methods to do this, so you can find one that suits you.

<figure class="tmblr-full" data-orig-height="1006" data-orig-width="1120"><img src="https://64.media.tumblr.com/2b63561ff34eb8e255054064edcbf3f1/34e6a002cedf6f29-f5/s2048x3072/8eba6767114c24387b8b4dd850f79341d557fa8c.png" data-orig-height="1006" data-orig-width="1120" data-media-key="2b63561ff34eb8e255054064edcbf3f1:34e6a002cedf6f29-f5"/></figure>

If the hash that you calculated matches the hash of the file listed on the website, then your version of the file is the same as the one on the server and it’s not been corrupted. We can see here that the SHA256 hash I computed does match, so the files are the same.

## Creating the Live USB:

To create the USB, the first step is to insert the USB thumb-drive you want to make bootable, and start up Rufus. It is important to note that part of the process is to format the drive, which will delete every file on it. **DO NOT KEEP ANY IMPORTANT FILES ON THE DRIVE, BACK UP ANY FILE YOU WANT TO KEEP.**

<figure class="tmblr-full" data-orig-height="538" data-orig-width="418"><img src="https://64.media.tumblr.com/53cf3274404dddb448963c82f0dfaf88/34e6a002cedf6f29-d5/s2048x3072/77977371de5f302b86f09314b882ca8a353ca3ac.png" data-orig-height="538" data-orig-width="418" data-media-key="53cf3274404dddb448963c82f0dfaf88:34e6a002cedf6f29-d5"/></figure>

Next you click ‘SELECT’, and navigate to the live .iso file you downloaded. After doing so, options for your live drive will be available. Most of these are advanced option, so for now you can ignore them, but you can change the name of the drive if you want.

<figure class="tmblr-full" data-orig-height="580" data-orig-width="418"><img src="https://64.media.tumblr.com/54cc00bfade938d55e5ff7ac76c88bf9/34e6a002cedf6f29-b6/s2048x3072/4f4d3bd7684497e98244fdcd9422aaa1fc5e1309.png" data-orig-height="580" data-orig-width="418" data-media-key="54cc00bfade938d55e5ff7ac76c88bf9:34e6a002cedf6f29-b6"/></figure>

After pressing START, you may receive some pop-ups. You can click through these, as the recommended options work. After clicking through the pop-ups, Rufus will start writing to the drive. You can now wait until it is finished, so read some more of your book or watch another film.

<figure class="tmblr-full" data-orig-height="580" data-orig-width="418"><img src="https://64.media.tumblr.com/a817ec10cdcc8de097997bb0b5733c45/34e6a002cedf6f29-f9/s2048x3072/f26ba791e0750914d7b11e41f3620dcc3a12e216.png" data-orig-height="580" data-orig-width="418" data-media-key="a817ec10cdcc8de097997bb0b5733c45:34e6a002cedf6f29-f9"/></figure>

Once it is finished, you can eject the drive. Your Live USB is now ready.

## Using the Live USB:

To use your live USB, first insert it into the computer while it is turned off. When it turns in, it should boot to a screen where you can select boot options.

<figure class="tmblr-full" data-orig-height="3024" data-orig-width="4032"><img src="https://64.media.tumblr.com/e5f7391ae67a9c0227c401fc38af8508/34e6a002cedf6f29-4a/s2048x3072/3ed73af549886ccd09ec4a74bc4c8d865555693b.jpg" data-orig-height="3024" data-orig-width="4032" data-media-key="e5f7391ae67a9c0227c401fc38af8508:34e6a002cedf6f29-4a"/></figure>

(sorry the quality isn’t great)

For basic use, you can select ‘Live system’, but there are more advanced modes that you can use. You can do some research to see what each mode involves, and which is best for a scenario.

After selecting out boot mode, our computer then boots to Kali.

<figure class="tmblr-full" data-orig-height="3024" data-orig-width="4032"><img src="https://64.media.tumblr.com/7b26126548125b6a8f96100dd64573ce/34e6a002cedf6f29-11/s2048x3072/e212cb83bb14728bca6536c0f8454c39da2cc5da.jpg" data-orig-height="3024" data-orig-width="4032" data-media-key="7b26126548125b6a8f96100dd64573ce:34e6a002cedf6f29-11"/></figure>

You may find, however, that when you try booting with the USB it boots to your native OS instead of Kali. This may mean that your BIOS (Basic Input Output System) is not configured to boot from the USB. This means that you will have to change your boot order from the BIOS. This is different for every motherboard, so you may have to look up how to do it for yours. Make sure that your BIOS boots from the USB before the hard drive.
