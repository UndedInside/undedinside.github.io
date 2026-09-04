---
layout: post
title: 'Creating Kali Virtual Machine: VirtualBox'
date: '2020-08-17T12:05:55+00:00'
tags:
- pentesting
- hacking
- kali
- virtualbox
- cybersecurity
- cybersec
tumblr_url: https://undedinside.tumblr.com/post/626713276216131584/creating-kali-virtual-machine-virtualbox
---
[Last time](/tutorials/virtual-machines-pt-1-kali-vmware.html) I wrote a guide on creating a Kali VM on VMware, but that isn’t the only hypervisor in existence. There is also VirtualBox (Which can be installed <a href="https://www.virtualbox.org/wiki/Downloads">here</a>)

The Kali image for VirtualBox is available <a href="https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-image-download/#1572305786534-030ce714-cc3b">here</a>, on the same page as the VMware image. Remember to install the right version depending on whether you have 32- or 64-bit Windows.

After installing VirtualBox, the home screen should look like this:

<figure data-orig-width="931" data-orig-height="572" class="tmblr-full"><img src="https://64.media.tumblr.com/01990a824f7ab676d0f02a8779565781/86fd4d09345910d8-30/s540x810/f428afcef0112c9bba924e26a0c83f587ac9e2a2.png" alt="image" data-orig-width="931" data-orig-height="572"/></figure>

Like last time, I already have a VM create, so you will be missing the “Windows” machine.

First, click import, and for file select the .ova file you just downloaded:

<figure class="tmblr-full" data-orig-height="754" data-orig-width="810"><img src="https://64.media.tumblr.com/5465534515f604abce4f41a85a8f5a5a/86fd4d09345910d8-9a/s540x810/b494fee54a4c432d5c1ab4981e8000918edccef2.png" data-orig-height="754" data-orig-width="810"/></figure>

After that, it will take you to a screen where you can change the VM settings.

<figure class="tmblr-full" data-orig-height="754" data-orig-width="810"><img src="https://64.media.tumblr.com/637af54f9c17bb4c4f9fc695c5419727/86fd4d09345910d8-d8/s540x810/8a0c6307adb55e243af743533f94e43bb894c23c.png" data-orig-height="754" data-orig-width="810"/></figure>

Click ‘Import’, then accept the license agreement. You should then see a progress bar while it sets up your VM.

<figure class="tmblr-full" data-orig-height="139" data-orig-width="522"><img src="https://64.media.tumblr.com/af796ccde0d3569d91b4880d3aae0fc9/86fd4d09345910d8-6c/s540x810/10153228fc171fc34229114b0abc4cb3d0d5e30f.png" data-orig-height="139" data-orig-width="522"/></figure>

Success! The VM has now been added to your list.

<figure class="tmblr-full" data-orig-height="572" data-orig-width="931"><img src="https://64.media.tumblr.com/2552119be72ae4ee0e0c73aba8e94668/86fd4d09345910d8-3b/s540x810/527870c66f1e29010ff61b948ca1616c9c3cc954.png" data-orig-height="572" data-orig-width="931"/></figure>

Simply press ‘Start’ to start your machine.

(note: I got an error when I did this, telling me I lacked USB 2.0 support. You can go into settings and disable USB 2.0 and the machine should start)

<figure class="tmblr-full" data-orig-height="1080" data-orig-width="1858"><img src="https://64.media.tumblr.com/39e2dbe10a315d031961d743d79fb5b4/86fd4d09345910d8-36/s540x810/eab8b9e4b2df734ad80a8926f56c68ab3f2a5ce5.png" data-orig-height="1080" data-orig-width="1858"/></figure>

You can press Right-Control F to toggle fullscreen, or you can keep it in a window.

Like the VMware machine, the default username and password are kali/kali

<figure class="tmblr-full" data-orig-height="1080" data-orig-width="1858"><img src="https://64.media.tumblr.com/8e2fab6aed31bf7525f5f480a5ab62d4/86fd4d09345910d8-c6/s540x810/297f0cfdfd8895e4cbe28efcd36d2fd130081d9f.png" data-orig-height="1080" data-orig-width="1858"/></figure>

Happy Hacking! Next post I will teach you how to make your machine more secure against hacking.
