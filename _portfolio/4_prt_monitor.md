---
title: PRT Monitor
description: Twitter bot 🤖 written in Python 🐍 that monitors WVU's PRT.
image: /images/portfolio/prt_monitor.jpg
tech_stack: [Python, Linux]
live_link: https://twitter.com/PRTMonitor
live_link_name: Twitter
source_link: https://github.com/rainerdeal/PRT-Monitor
source_link_name: GitHub
---

#### Dependencies:
* Coffee ☕️
* [Twython](https://github.com/ryanmcgrath/twython){:target="_blank"}

#### Background
PRT Monitor is a Twitter bot that tracks the uptime/downtime of WVU's PRT and helps users stay updated on whether it is running. The PRT is an elevated tram car system for public transit and is located throughout Morgantown, WV. It is used by locals and students to get around campus or the city itself. The goals of the system were to minimize traffic and provide an alternative public transportation option. Morgantown, like much of West Virginia, has unique geographical and weather limitations, making a non-traditional public transit system necessary. 

Check out this cool historical snapshot of the PRT [here](http://www.boeing.com/history/products/personal-rapid-transit-system.page){:target="_blank"}.

Despite how effective the PRT is in Morgantown, it is not perfect. There are only 5 stations to board the PRT, so commuters need to travel some distance before or after their PRT ride to complete their trip. It is not uncommon to walk about 15 minutes to the nearest station, only to find out that the PRT is temporarily out of service because of weather. Before PRT Monitor existed, the best way to find out whether the PRT is running was by following the official twitter account or checking the status on the website, but these sources do not report each outage. Typically they only announce an outage if it is expected to be longer than 30 minutes of downtime.

PRT Monitor will report any outage as long as it lasts at least 5 minutes, and because it is a twitter account, users can receive push notifications instead of manually checking a webpage. The goal of the project is to help commuters save time in their busy schedules by letting them know about service outages *before* they get to a station.

#### Details
The project is entirely written in python and is running on a [Raspberry Pi 3 Model B](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/){:target="_blank"} in headless mode. The scripts are triggered by [CRON](https://en.wikipedia.org/wiki/Cron){:target="_blank"} and I use a [Twitter App](https://apps.twitter.com){:target="_blank"} for the tweeting functionality. You can see PRT Monitor in action on [Twitter](https://twitter.com/PRTMonitor){:target="_blank"}.

#### What does it do?
##### PRT_Monitor.py
Every 5 minutes this requests the PRT status from a JSON feed. If the status is different than the last status, then it will record the new status in a CSV file and tweet the new status.

So this doubles as both the twitter bot and the "monitor" at the same time.

##### PRT_Analysis.py
This script is executed every Friday at 5pm. And here is what it does:
  1. Adds up how many times the PRT has gone down during the semester.
  2. Calculates the amount of time the PRT was out of service (doesn't include when the PRT is closed).
  3. Calculates the amount of time the PRT was working normally.
  4. Calculates the percentage of uptime.
  5. Tweets the stats in a pretty format.

> You're welcome to check my math (was never particularly good at it). 😬

##### PRT_Prediction.py
This one is just an idea I had. It doesn't work yet. But I was thinking that I could predict outages based on historical data and weather.