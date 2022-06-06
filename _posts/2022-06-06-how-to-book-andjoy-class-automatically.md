---
toc: true
toc_label: "Contents"
title: How to book andjoy classes automatically
tags: [node, andjoy, fitness, class, crossfit]
excerpt: When going to crossfit in the "rush hour" you only have a small time frame to book the class. In 30 minutes all the slots can be full and you can't go anymore. With this script you will book all the classes you need automatically.
header:
  teaser: /images/gitlab_andjoy.png
lang: en
ref: book-andjoy
---

## The problem

In most gyms/crossfit places, for some activities, you have to book them since there is a limited amount of people that can go. In my case, I tend to go at 7pm and I can start booking since 48h before. If you forget to book it, in around 30 minutes the class is full and you can't assist anymore.

I had tried to put an alarm, a todo list item, eveything...but sometimes I'm far away from technology at 7pm on a Saturady and then I miss the the booking "time frame".

Not anymore, meet the "andjoy autobook script"

## Looking for a solution

Using AndJoy via web I realized there is an API I could call to book the classes.

![andjoy web API call example](/images/andjoy_web.png)

I started playing with Postmand and quickly replicated the calls I needed. There are two:

1. `events` - `POST` - Will give me the events for a given day and time frame.
1. `bookings/book` - `POST` - With the event Id retrieved in the previous call, I will do the booking

Knowing which calls to do, next step how can I run them automatically? I quickly thought about a node script in Gitlab.

Why? Node scripts allow to make API calls easily and Gitlab has scheduled builds that work really well in my experience

## The script

I uploaded the script to a repo: [andjoy autobook class](https://gitlab.com/jpallares/andjoy-autbook-class). I'm not winning any naming contests. The key is to use it to initialize the env variables with the corresponding values. Being the Cookie the most important, otherwise you won't have access rights.

To retrieve it look in your browser network traffic when using AndJoy via web.

![andjoy cookie example](/images/andjoy_cookie.png)

Finally, let me show you and example of a successful booking:

![gitlab successful build](/images/gitlab_andjoy.png)

I hope you enjoy it and I hope you don't go to the same crossfit as me 😃
