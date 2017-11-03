---
layout: post
title: "Insert Internal Tool Details Here"
description: "This is a retrospective post about my experience and learning from working on an internal tool that didn't go quite as planned"
date: 2017-11-3
updated: 2017-11-1
comments: true
categories: internal
tags: [retrospective, internal]
---

TODO: add architecture diagrams and some code snippets

On your first day you go to orientation, meet your manager, and get your computer ready for use. On your second day you sit in on a meet discussing a project you'll be joining right away. Or at least, that's how it went for me on my first day of my first non-internship non-coop job in tech!

The project happened to be starting its first(1) sprint on the week I started, so the timing couldn't have lined up better. While I didn't have as much time for training videos as I expected, I'm not concerned with missing out because being somebody who is probably addicted to learning means that I will likely gravitate towards upskilling anyway. However, for the time I was on this internal tool, I didn't really have much time to work on anything but the project because of a strict deadline paired with nothing more than a vague idea of what needs to be done.

For this post, I will pretend we are reviewing a timeline and add commentary on what I was thinking at that time. This is an exorcise for myself to learn where the warning signs started and how I can take what I already knew at any given moment and make sure that the next time I find myself in a similar situation I know how to handle it. So, let's begin.

# Phase 1: It's a crud app so nothing matters

This is the mentality that I noticed people taking at the beginning of the application. The first meeting on my second day of work had all the stakeholders together planning out what features the app should have, but the app had been in the works for about 8 months in the design phase, so this meeting was only an hour long.

## The technology

For the first day or two we divided into two groups - those working on the backend and those working on the frontend. Because I said my experience was with web APIs, I was asked to join that team as we were planning to make a Web API initially. The frontend team planned to use React as that was their experience, so there would be communication between a C# Web API and a React frontend that both teams would need to plan together.

This plan did not last long, as it was decided that it was too complicated for our solution. We quickly shifted to using MVC and putting all the logic in one C# solution.

## My opinions then and now

I found it interesting that our introductions of what we have used before were reused as our choices for what we want to work on. As a learning addict (this is not a real thing as far as I'm aware, I am 100% self diagnosed) I would have leaned in the other direction if it were up to me. Retrospectively I understand that this was done this way because of the short timeline to get this project presentable.

I don't like to treat anything as just a crud app when it comes to architecting a solution because I have been burned before. Especially when I don't have the business requirements and won't have them in the near future - in this scenario I would personally architect the solution to be as scalable (and therefore as modular) as possible. From my previous experiences, expecting that nothing will need to scale up and it's all just a crud app always just ended up in more complexity. So, I tried to find a way to suggest other solutions but did not do so effectively. Because it was my first weeks here as a full-time employee, I was not aggressive at all after providing my opinion and letting the team do with it what they wanted. Retrospectively, I will try not to make this mistake again.

# Phase 2: Expansion

We suffered from a lot of scope creep, and rearchitected our solution every time it started to get too complicated for the exiisting solution. We stuck to MVC the whole time but broke up the solution into sections (first we separated front and back end, then we separated out more layers). This was much more manageable given all the new features we decided to support by this point in the project.

## My opinions then and now

Again, I just wanted to go in the opposite direction - start as modular as possible and maybe condense if needed. Every time we expanded our solution I got more excited because we were moving more in the direction I wanted to go. I accepted that starting with a modular solution may be ideal but with this timeline it isn't possible. However, it was becoming apparent that we ended up spending more time recovering from issues raised by starting out small than we would have spent by just starting big in the first place. This is exactly what I expected, so at this point in the project I was starting to get frustrated. I love learning things for the first time; relearning is much less fun.

# Phase 3: An ideal solution

In this solution, we would be using serverless azure logic apps, and a React frontend. This solution would have every user story implement its own logic app and anything else needed, so there is a high probability of code repeating but it's much more extensible.

## My opinions then and now

Following the trend of me liking the project more and more as time goes by and we make the solution more and more modular, I love this approach and am sad we never got to implement it. It took a while to wrap my head around the idea of code reuse being acceptable in an ideal solution, but I understand it in the scenario that we want as much modularity as possible. It was explained to me that the more code we reuse across functionalities, the more coupling we have, the more work we have to put into adding new features.

# Conclusion

You can't chose a non-scalable solution architecture and try to effectively adopt an agile workflow. You just can't.

# Key

(1) My whole time on the project (two months) felt more like one sprint with multiple iterations than actually building multiple sprints.