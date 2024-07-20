---
title: "My personal tech stack, 2024"
tags: [ tech ]
layout: post
---

Today's TIL: some people have PC trouble that lasts for years, a sort of daily grind of not-quite-rightness with their PC. And some other people don't.
I'm in the latter category, so this post is an attempt to record what my setup is and general principles of "PC hygiene".

- [Hardware](#Hardware)
- [Operating systemi](#OS)
- [Applicationsi](#Applications)
- [Preferred apps](#Preferred apps)

## Hardware
There is always a temptation to blow serious coin on a dream laptop. But realistically, that power would sit idle 80% of the time.
I'm not training AI models every day of the week, and frankly, when I need that sort of horsepower I can fire up what I need in the cloud for exactly as long as I need it. And since my gaming is done on a PlayStation, I'm free and clear of the main reasons to drop $$$. 
My PC budget is very lean, and I like it that way. Perhaps related, I am not testing out some bleeding-edge hardware and exercising new bugs. All ther drivers on my PC
have already been through several rounds of updates by the time I get the hardware.

My 2024 choice is a refurbished Dell Latitude 7490, which cost me [$400](https://www.pcliquidations.com/dell-refurbished-laptops) and is a *joy* to use: it's very light, it's fast, and Windows
runs very smoothly. 

There's a lot to be said for buying a "corporate" laptop from the world's #1 PC maker. You just know that Microsoft and Dell will have made very sure that it runs well because they share the same corporate customer base. This isn't some consumer-grade gamble from Costco. My 2024 buy is actually a replacement for the same model that I had as my work PC for five years prior: when 
I surrendered that machine to my IT people I immediately went and bought another for personal use. 
16GB RAM, Intel i7 CPU, 500GB of storage, and real ports: Ethernet, audio, USB, Thunderbolt, and full-size HDMI. 

## OS
Surprise, Windows. Windows 11 Pro to be exact. Pro is preferable over Home because the former includes whole-disk encryption via
BitLocker. (If you are following along: just make 1000% sure that you know what your recovery key is.) Plus, Pro includes better virtualization support, which 
is something that makes me feel like I could virtualize something if I needed it (although to be honest with myself, there have been
better solutions to that problem for a while now).

I'm firmly in the Windows camp for one reason only: 365 native apps like Word and Excel. Sure, there are web versions, but try opening
a long document or a complex spreadsheet. Native is better. 

## Applications
There are at least six (six!) ways to install software on your Windows PC:

 - Use the app installer from the supplier's website. For example, go to adobe.com and download Acrobat.
 - Install the app from the Windows Store.
 - Sideload the app using PowerShell or DISM.
 - Download the app in portable format, e.g. from [Portable Apps](https://portableapps.com/) and run it from a folder of your choosing, such as a USB stick.
 - Use scripted installs from the app supplier, such as MSI packages.
 - Use meta-installers that wrap the app in a package manager.

Unsurprisingly, after a few months of use, most PCs are cluttered with all kinds of weird cruft as a result of adding and removing apps.
I assert that cruft is the #1 reason why PCs degrade over time. 

 - **Recommendation**: remove every last bit of optional software that Microsoft throws at you before you do anything with your PC. 
 
 I get rid of the Candy Crush, Solitaire, Photos, Clock, XBox and all the other fluff. They're basically teaser apps that try to drive users to the Microsoft app store anyway, but I don't need that stuff. All of it gets removed via the Add/Remove programs dialog.

 - **Recommendation**: be utterly ruthless about what you choose to install. The best software is no software. The best package is the lightest, least invasive one that completes the task you wanted.

For example: WhatsApp and Discord bug me all the time to use their app instead of the web versions. But that's more stuff on the disk, more cruft in the Registry, and just more fluff all over for very marginal gains. Nope, I'll stick with the web versions, thankyouverymuch.

 - **Recommendation**: use a meta-installer for anything that you install. No exceptions.

Think of a meta-installer as a tool that understands all the apps out there and their quirky way of being installed. It then hides all that  and presents a single style of adding, maintaining, and removing apps. It is, to put it mildly, a huge improvement. 

I like [Chocolatey](https://docs.chocolatey.org/en-us/why/), which allows me to type things like 
>`choco install dropbox`	*# install Dropbox*
`choco upgrade all` 		*# upgrade all apps* 


## Preferred apps
For 2024:
 - **For productivity**: [Office 365](https://www.office.com/). Sorry web, sorry Google Docs, sorry LibreOffice, but you will pry 365 out of my cold, dead, hands. There is simply nothing like real Excel.
 - **For video calls**: [Zoom](https://zoom.us/). Teams in corporate-land is (ignore the haters) very, very powerful, and only getting more so as Microsoft throw more at it. Teams for home users is a pale shadow of that beast and doesn't hold a candle to Zoom.
 - **For notes**: [Notepad++](https://notepad-plus-plus.org/). Text editing, note taking, and generally acting as a Swiss Army knife tool 
when I need to manipulate some data. Note-taking apps are a deeply personal decision but after years of trying all kinds I've concluded that 
simpler is better. The web ones tend to degrade over time (enshittification, etc.) Moreover the really important things about a note app are that it runs offline,  it starts and runs so quickly that it doesn't get in the way of your thoughts, and that it doesn't lose your notes. So buh-bye to OneNote, EverNote, and so on.
 - **For development**: [WSL2](https://learn.microsoft.com/en-us/windows/wsl/about) (Windows Subsystem for Linux). Remember I said their were better solutions than virtualization? Well, this is one. Gives me a full Linux environment
   that lets me do git, code, editing, and anything else I can think of. (OK, there is virtualization going on under the covers, but with no effort on my part). 
 - **PDF reader**: [SumatraPDF](https://www.sumatrapdfreader.org/). Adobe Acrobat is the de facto standard for PDFs, but that program tries and fails to do too much: I want to read PDFs, not be told that half the buttons on the
screen won't work unless I upgrade to Adobe Cloud. SumatraPDF is faster to start up, faster at rendering long documents, and gives me exactly zero problems. 
 - **For backups**: [OneDrive](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage) and [Dropbox](https://www.dropbox.com). As a file sharing service, OneDrive for consumers is...meh. As a seamless backup service, it's very good. My PC could blow up tomorrow, I could have a replacement in three days, and my Documents folder would hook up to OneDrive and I'd be back in business. The nit is that cloud services have a habit of evaporating overnight. So, Dropbox is my archival service, *just* in case.
 - **Security, Anti-virus** etc: Microsoft's own suite is perfectly adequate for your PC. Ignore the desperate calls and back-handed attempts by some vendors to get you to install their stuff. Trust me, once you sign up for a 30-day trial of anything, that cruft is never leaving your PC. Avoid.
 - **Web browser**: [Edge](https://www.microsoft.com/en-us/edge) with [uBlock Origin](https://ublockorigin.com/) and [BitWarden](https://bitwarden.com). Edge does some skeevy things, like continually trying to populate my home page with fake news stories of the  "this one weird trick" and "you'll never believe what..." kind. But, it comes with Windows, supports plugins as well as Chrome, and runs very well on battery power when I'm unplugged. So, in keeping with the less-apps-installed-is-better rule, it gets a place. uBlock Origin is absolutely mandatory for all web browsers: Firefox, Chrome, Edge, whatever. The modern web is a cesspool of ads and it's a much calmer and faster experience to browse the web when you're not losing whole chunks of your screen and your attention to ads.

So there you have it. Pick decent but cheap hardware, run as little a possible on it, and keep track of what you install. Got a suggestion for 2025's stack? Let me know.
