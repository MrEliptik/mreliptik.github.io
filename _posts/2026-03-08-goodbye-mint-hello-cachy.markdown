---
title: "Goodbye Mint. Hello Cachy!"
layout: post
date: 2026-03-08 08:00
image: /assets/images/mint_cachy.jpg
headerImage: true
tag:
- linux
category: blog
author: mreliptik
hidden: false # don't count this post in blog pagination
description: I ditched Mint for Cachy and I loved it
---

About a week ago, I made a [video](https://youtu.be/_7SPrf1VKg4?si=TIHMiWsK-gZbHdP_) about my Linux experience. I'll let you watch it if you haven't already, but let me 
summarize it for you:
- I tried to daily drive Mint
- Linux is wonderful, and I want to use it
- For the most part, it works flawlessly and even better than Windows
- I got small issues, most of them not horrible but annoying (bluetooth not connecting correctly for example)
- Device support can be messy, and relying on user-made apps is not ideal (streamdeck)
- I can't run Affinity Designer 2 and that's a big issue for now as I need it for [Hyperslice](https://s.team/a/2977820) and [Lexispell](https://s.team/a/4053960) but I want to find an alternative for the future.

That sums up my experience, and unfortunately, this means I'm often using Windows mostly because I need to work with 
Affinity. Also, everything is set up there, so it's just easier even if the experience sucks.

I'm writing this to document the progress, as I'll probably do an update video in the future, where I hope to be able 
to say I'm fully daily driving Linux.

### Fedora was the spark

I received plenty of comments on this video, and many suggested using more "bleeding edge" distros like Fedora or 
Arch. I quickly decided to give Fedora a go on my laptop, and I enjoyed the process. While I'm not a total fan of KDE, 
I have to admit I prefer it to any other DEs out there.

It seemed to run smoothly, sleep was better handled, and I just liked the overall proposition. KDE is good enough by 
default, and I can take the time to customize it if I ever need to. I ran Fedora on my laptop for a few days and was 
starting to get the itch to give Linux another proper go on my desktop. I just hate Windows at this point, and I'm 
really fed up with it, so I want something new.

### Enters CachyOS

On Thursday, I ended the day in a bad mood. I was not as productive as I wanted, and I felt like I was going nowhere. 
This made my itch grow even stronger, and I just decided to wipe Linux Mint and give CachyOS a try at 10pm. In 
hindsight, this is slightly stupid, but I don't regret it.

The installation went super smooth, and everything worked out of the box. I feel like the recommendation we were 
hearing a lot, that PopOS is good because it has Nvidia support out of the box, is kinda dated now. Both my Fedora 
install and Cachy but even Mint came with Nvidia drivers. It was slightly more complicated on Mint, but incredibly 
smooth with the others, meaning I did nothing and it just worked.

The first impressions with Cachy were great. It's incredibly responsive, Bluetooth works well (it wasn't on Mint), and 
all my devices are recognized without any issue. I went with KDE and after some work, I think I found the amount of 
customization I like. The other advantage is that KDE comes with a bunch of software that are pretty useful, like a 
spotlight-like search bar, KDE connect, a nice screenshot/recording tool, etc...

After the first impressions comes the reality. Because Arch-based distros are maybe less popular or mainstream, some 
applications are not available. It appears to be pretty rare so far, and most of the time you can fix it using the 
AUR, which I believe is packages made from the community, so less "official"? One example is [Espanso](https://espanso.org/), a snippet tool, 
which doesn't even have appImage for Arch. This meant I had to compile it, but it was literally just installing Rust 
and then compiling. Two lines of code in total, which I'm ok with. With other software, it was slightly more 
complicated, like with OBS where the default package doesn't have browser support which is essential for streaming. I 
tried a bunch of installs, and I finally decided to use the obs-studio-git from the AUR which is the latest commit. It 
might be risky for stability, but at least I have everything. There was still a problem preventing browser docks to be 
available because of Wayland... I'm not going into the details, but I was able to run it using XWayland. I hope it's 
not going to break, but we'll see in the coming weeks.

Wayland is cool, but it seems like it might still be a problem for some apps. Even Godot only added game embedding for 
Wayland with the latest 4.6 release. I don't know the whole history, but it seems like Wayland has been the X11 killer 
for so long now, and yet so many things can still go wrong. KDrive also behaved badly because of it, at least the 
login screen. Again, I was able to make it work by forcing it to use it something else. It seems I'm quite lucky, 
though, as everything appears to be pretty mature and stable outside of that.

I still have some work to do to make my Stream Deck behave nicely, and I think I just have to kill the idea of having 
it be a 1-to-1 replica of my Windows setup. It's just going to be less good for now. It's pretty painful because 
having a nice setup makes streaming much easier, but I'm sure with enough patience I'll have something decent.

The last big problem is still Affinity, unfortunately. I managed to install it using [some guide](https://github.com/seapear/AffinityOnLinux), and it runs with Wine 
but the performance with a real-life document and not just an empty one with a text box is horrible. It's basically 
unusable. For now, I didn't have the energy to tinker more with it. I already spent a lot of time trying to get it to 
just work. I'd love to be able to run it, as it would allow me to not switch to Windows for work, as it's the only 
real missing piece.

### Am I going to distro-hop?

While it's very tempting to switch to a new distro with the hope of it fixing everything, there are very few 
differences between all of them. Unfortunately, Elgato not supporting the Stream Deck on Linux will not be fixed by 
trying another distro.


Considering how painful and time-consuming it is to change OS, I hope this is the last time I'm switching. There's 
something fun about discovering a new OS, new languages, or anything new. But it wears off fast. Once you're left with 
real problems that are sometimes unsolvable, you feel empty and hopeless again. I think there are plenty of benefits 
in committing to something. Just like we commit to ideas or relationships. It's tempting to seek the greener grass, 
but it's probably better to accept the problems and try to work with them.

See you soon for another Linux update!
Eliptik