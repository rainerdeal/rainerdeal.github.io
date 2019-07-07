---
title: 'AI: Image Recognition'
description: Image Recognition AI trained to detect road signs.
image: /images/portfolio/opencv.png
tech_stack: [Python, OpenCV]
live_link: null
live_link_name: null
source_link: https://github.com/dmbuck32/AITermProject
source_link_name: GitHub
---

#### Dependencies
* Coffee ☕️
* [OpenCV](https://opencv.org)

#### Background
This was a group project I worked on for an Artificial Intelligence class that I took my final year at WVU. Our goal was to train an AI to recognize common road signs. We were able to run a live demo in class by having a group member drive around in Grand Theft Auto V and running our AI in the background. You could observe the AI highlighting and correctly labeling the road signs in the game.

#### Details:
We used an open source python library (OpenCV) for training the AI to recognize road signs and we found an open source library of road sign images that we could use. We had to do extensive pre-processing on the images to prepare them for our AI's consumption. Once the images are prepared, we can run the training scripts. This was the most time consuming part of the project as it pushed our computers to the limit and required a lot of trial and error. The final step was to create a basic UI to control the AI. We added language selection and sliders to tweak the sensitivity. We had to be very careful of our settings so that we could run the game and the AI together on one machine. 

#### Features
* Language selection:
  * English
  * French
  * Spanish
  * Japanese
* Recognized Signs:
  * Merge
  * Added Lane
  * Pedestrian Crossing
  * Lane Ends
  * Stop
  * Stop Ahead
  * Signal Ahead