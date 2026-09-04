---
layout: page
title: 'Creating Kali Virtual Machine: VMware'
date: '2020-08-17T09:30:54+00:00'
tags:
- pentesting
- hacking
- kali
- virtual machine
- vmware
- guide
- linux
- linux tutorial
tumblr_url: https://undedinside.tumblr.com/post/626703524023189504/creating-kali-virtual-machine-vmware
---
This is a guide on how to create a Kali Linux virtual machine using VMware. Kali Linux is a ‘distribution’ (or version) of Linux which comes preloaded with many tools useful for hacking/penetration testing.

The first step is to download VMware Workstation Player. This can be found <a href="https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html">here</a>.

Once you have downloaded VMware, you will need a Kali ‘image’, which is a file containing the operating system. You can download one for VMware <a href="https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-image-download/#1572305786515-43ed3ee1-b9c8">here</a>. make sure you get the right one for your Windows architecture (You can find if you use 32- or 64-bit windows <a href="https://www.lifewire.com/am-i-running-a-32-bit-or-64-bit-version-of-windows-2624475">here</a>). It should download as a .zip file, so you will have to unzip it. After opening the folders, you should have files looking like the following:

<figure data-orig-width="1693" data-orig-height="882" class="tmblr-full"><img src="https://64.media.tumblr.com/563b0a2dd537574a999c8f5e85b861c3/1551d3ea1391e39d-d9/s540x810/d9c26c1fbf66e8a190f6c64febe2a625be71f6ba.png" alt="image" data-orig-width="1693" data-orig-height="882"/></figure>

When you open VMware Workstation Player it should look like this:

<figure data-orig-width="700" data-orig-height="561" class="tmblr-full"><img src="https://64.media.tumblr.com/9360ffc07a3827da1d5e4b42fa366d4c/1551d3ea1391e39d-af/s540x810/c944056a2d4ae0343a2401d8019c3f64abc34a0a.png" alt="image" data-orig-width="700" data-orig-height="561"/></figure>

Here I already have some VMs installed, so on your version it should be missing TryHackMe and Ubuntu (Note: TryHackMe is a website for practicing hacking, it is not an invitation to hack me). Next we’re going to click ‘Open a Virtual Machine’ and navigate to the folders we unzipped earlier. You should only see one file:

<figure data-orig-width="946" data-orig-height="533" class="tmblr-full"><img src="https://64.media.tumblr.com/66c508d81164d32c392bb7d1eb7e1d81/1551d3ea1391e39d-d6/s540x810/fa95dd07b307a0acbe9106a2ad720fcc1f49812d.png" alt="image" data-orig-width="946" data-orig-height="533"/></figure>

Double click that file to open the Kali VM. You should see the new VM on the home screen of Workstation Player.

<figure data-orig-width="700" data-orig-height="561" class="tmblr-full"><img src="https://64.media.tumblr.com/9f203d42ecb1cc92378b435ed70bdf39/1551d3ea1391e39d-a9/s540x810/4bb535f71ac601cc70637e6744ebe83720aa1276.png" alt="image" data-orig-width="700" data-orig-height="561"/></figure>

You can right click on that VM to rename it, or to change the settings. Let’s change the settings.

<figure data-orig-width="704" data-orig-height="657" class="tmblr-full"><img src="https://64.media.tumblr.com/d6ef7f84206534d1a2d7ff0a100a5080/1551d3ea1391e39d-20/s540x810/6fcff10ca6064a89f42b50ddb412c1c0e7b4d4f7.png" alt="image" data-orig-width="704" data-orig-height="657"/></figure>

Let’s leave the memory at the recommended amount (This may vary depending on your computer). I normally change the Network Adapter to ‘Bridged’ but you can play around and see what fits you better. We are also going to leave every other setting at the default.

<figure data-orig-width="706" data-orig-height="689" class="tmblr-full"><img src="https://64.media.tumblr.com/fa8a064af51983435090d580f330da7a/1551d3ea1391e39d-25/s540x810/2b4fe41ce34b9f4ac86620d16f80c5bc63de2452.png" alt="image" data-orig-width="706" data-orig-height="689"/></figure>

Now click ‘OK’ to go back to the home screen, and then click ‘Play virtual machine’ to start your Kali machine.

<figure data-orig-width="700" data-orig-height="561" class="tmblr-full"><img src="https://64.media.tumblr.com/eb4fa224d0859c0d43dfa96f9113ddf6/1551d3ea1391e39d-9f/s540x810/49edd81acbdd41c4bc685554dc2462894f965e62.png" alt="image" data-orig-width="700" data-orig-height="561"/></figure>

If you see this screen, just click ‘I Copied It’.

After some loading screens you should see a login page.

<figure data-orig-width="1282" data-orig-height="785" class="tmblr-full"><img src="https://64.media.tumblr.com/24d731ff208b9d4aa4bbf5970b814f79/1551d3ea1391e39d-74/s540x810/3f45869a787fe3451d199c97dd2f01e316ab5ca7.png" alt="image" data-orig-width="1282" data-orig-height="785"/></figure>

(Depending on the version of Kali installed, it may look slightly different)

The default login credentials should be ‘kali’/’kali’, but if this doesn’t work you should look on the Kali site to see if they have changed. You should now see a screen like this:

<figure data-orig-width="1282" data-orig-height="785" class="tmblr-full"><img src="https://64.media.tumblr.com/d744a130ddf41d912b5c57214cbc5506/1551d3ea1391e39d-bb/s540x810/019f40b1f4aeac5e476439476008bb12f0a5979a.png" alt="image" data-orig-width="1282" data-orig-height="785"/></figure>

Congratulations! You have now deployed a virtual machine. You can find a post explaining how to secure your new VM against being hacked <a href="https://undedinside.tumblr.com/post/626894162165432320/securing-kali-against-hacking">here</a>
