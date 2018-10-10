---
layout: post
title: The Ghost of Harrenhall
date: 2018-10-10
image_path: images/motoko_kusanagi.jpg
categories: []
tags: []
---

## What does it do?
### PRT_Monitor.py
Every 5 minutes this requests the PRT status from a JSON feed. If the status is different than the last status, then it will record the new status in a CSV file and tweet the new status.
