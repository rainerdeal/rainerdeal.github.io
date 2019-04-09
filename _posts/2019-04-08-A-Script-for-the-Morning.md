---
title: A Script for the Morning
date: 2019-04-08
soundcloud: https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/389104506&color=%23ff5500
tags: [shell, script, scripting, morning, routine, bash]
---

Not long after I started working as a software engineer, I noticed that I always open up the same apps for work and put them into the same order on their respective desktops. It was getting tedious.

I'm the type of person that likes to optimize things. If I'm playing a game, I'll try to min/max as much and as quickly as possible. If I notice I start to repeat something, I try to automate it. 

Opening up applications to start your day at work isn't that big of a task to automate, but I did it anyway, and now I use it almost every day!

###### work.sh
```bash
#!/bin/bash
# Script to open all my work apps and start my day.

echo "Hope you have a fantastic day Ricky! 😊  Starting your work apps..."

open -a "Safari" https://www.messenger.com https://confluence.marriott.com/#all-updates https://atlassian.marriott.com/secure/Dashboard.jspa
open -a "Microsoft Outlook"
open -a "Spotify"
open -a "Messages"
open -a "Skype for Business"
open -a "Microsoft Teams"
```

It's a pretty simple and straightforward BASH script with a silly message. The Safari line is especially cool because it opens three tabs and loads those three sites.

After writing the script, you have to make it executable using the command:
```bash
chmod +x work.sh
```

To start my day, I CMD-space `Terminal`, `cd Documents`, and run `./work.sh`. You can save this executable in a number of different places, but I just left it in Documents. The next step would be to create an alias so I can just say `work` instead of `./work.sh`.

So this just quickly opens all the work apps and throws them onto whatever Desktop I'm on at the time. Then I have to use my mouse 🤮 to move them to their correct Desktops. Well today I learned that if you organize all the apps the way you like them, you can right-click their icons in the Dock and assign them to a Desktop. Now when I open my apps they go right where I want, no mouse required!