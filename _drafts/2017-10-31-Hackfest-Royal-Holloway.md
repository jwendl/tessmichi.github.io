---
layout: post
title: "Hackfest Royal Holloway: Detecting Illegal Gold Mines in Ghana"
description: "For my first hackfest, I working with a team of Microsoft engineers and a PhD student at Royal Holloway to detect illegal gold mines in Ghana."
date: 2017-10-31
updated: 2017-11-1
comments: true
categories: ML, hackfest, first
tags: [ML, machine learning, hackfest, first]
---

# Background

The goal of the project is to help out a PhD student who is working on studying the ecomonic implications of illegal small scale gold mining on the populations nearby, and our goal as microsoft developers was to spend a week creating a deep learning model to find said mines. Using satellite images, we set out to detect precise locations where the mines exist. By the end of the week, our success is measured on whether or not we were able to detect, correctly, which images from a large store of satellite imagery show illegal small scale gold mines.

# Why I chose it

I started working at Microsoft in August, 2017, and spent most of my time working on an internal tool (it took up almost all of my time from my second day until last week). My manager told me to choose a hackfest or other collaboration event to be a part of, and this "Detecting Illegal Gold Mines in Ghana" caught my eye because I have never programmed with machine learning other than the rule based stuff I did in classes at Drexel. I did get to study some theory behind image processing, and one paper caught my eye about how to take street level images and determine where in Europe they were taken based off of the style of things like street lamps, window panes, etc [TODO link this paper]. So I found it really exciting to get to take this to a whole new level - using birds eye images and parse their content to determine what's in them - and actually get to do some prac

# What I wasn't prepared for

My computer doesn't have an nvidia gpu, which it turns it is really helpful for ML projects. With all this image processing, using the gpu to get the work done really makes a difference. I ended up using VMs to run the code.

# How we tackled reaching our goal

By breaking up into groups such that only half the developers were working on the main goal, and the other half worked on making sense out of the economic data collected by the student. In hindsight, we should have probably had everybody work on the main goal.

## Why we are only detecting gold mines in Ghana

Because that's how we trained the algorithm. In machine learning, you have to decide how specific you want to get when training a model and stick to it. You cannot, for example, train a deep learning model using only images of Ghana and expect it to work around the world. Neither can you even train it using images from half of Ghana and expect it to work on all of Ghana.

# To read about the project

Take a look at the blog post we created about it here: 