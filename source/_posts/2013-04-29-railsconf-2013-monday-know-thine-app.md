---
layout: post
title: "Know Thine App"
description: "Know Thine App"
category: Presentation
tags: ['RailsConf 2013']
---

## Summary

This was a "marketing" sell for a new **Tilde** product: **Skylight**, a Performance Measurement Utility.
The purpose is to give you a tool for rapidly
detecting, isolating, and fixing performance hiccups in your application.

<!-- more -->

I did sign up for the beta.

### Pros

* Shows promise in isolating causes even on rare problem events.

### Cons

* Yehuda Katz obviously rushed this presentation.  Too much repetition of "long tail" Web responses;
not enough time
on his
product.
* He tried to differentiate **Skylight** from New Relic; I'm not sure he succeeded.

## Raw

About measuring your app.

How do you validate your hypothesis?

You need to measure anything that has value.

Which Line is Slow?

Developers are paid to add business value, not write code.

Need a correct model model of how code is running by production delivering business value.

Business value is the measure $ earned and compare it with historical data.  Use tools to detect thresholds.

* users that add items to the shopping cart
* items added
* items removed
* users checking out
* successful orders

Need analogous measurement for developer.

so, need to *measure it*.

Performance is business value.

An average measurement is not a great metric.

 * mean (average)
 * median (middle)
 * standard deviation (variance)

 We mistakenly think that we only have to worry about values clustered around the mean.

 Average salary, for example, doesn't fit.  If we focus on the middle, we miss a large chunk of reality.

 Web responses are "long tail".

wonkish: log-normal-distribution
