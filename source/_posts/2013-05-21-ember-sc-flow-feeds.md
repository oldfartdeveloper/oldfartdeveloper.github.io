---
layout: post
title: "Ember SC Flow Feeds"
description: "Ember-SC"
category: Presentation
tags: [Ember-SC]
---

Speaker: Ben (ben@nerdyworm.com)

# What?

A video player implemented in Ember.

<!-- more -->

# Why?

* Too many RSS feeds :(
* Video Playlists
* New music everyday

Wanted to create an Ember demo app.

# flowfeeds.com

* Stack
    * Ember.js & Rails 4
* Features


# Audio & Vdeo

* LIbraries
    * Video. YouTube JSAPI
    * Audio: SoundManager2

The two APIs are completely different

Author uses a facade called a PlayableController

Is using `Ember.K` to set up abstract method that the two "real" controllers subclass and implement.

Source: github.com/nerdyworm/flowfeeds
contact: ben@nerdyworm.com
