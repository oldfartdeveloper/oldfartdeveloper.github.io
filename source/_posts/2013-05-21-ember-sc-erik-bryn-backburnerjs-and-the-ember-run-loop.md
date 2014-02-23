---
layout: post
title: "Ember SC Backburner.js and the Ember Run Loop"
category: Presentation
tags: [Ember-SC]
---

Speaker: Eryk Bryn

## Summary

How Ember JS's 'run loop' works.

<!-- more -->

## Pretalk

Erik Talked about his history w/ Ember.  He was a Rails developer that was doing more and more Javascript work.

Was sold on Yehuda's talk about templates.

### The Great Divide

Do you do all Javascript instead of HTML?  SproutCore did this.

But EmberJS leverages HTML, which is becoming more powerful.

Javascript is powerful enough to make web applications like native applications.

Serious Javascript development with Ember; feels fortunate.

# Talk

## Backburner.js

Is a micro-library that now is the Ember Run Loop.

## What Does the Runloop Do?

It's a queue.

Erik: all about coalescing.  Keeps the DOM from being updated unnecessarily.

Ember hides BackBurner from you.

Run loop is a set of queues:

* sync
* Actions
* render
* afterRender
* destroy

Libraries can add their own queues

### Sync

Is for synchronizing bindings.

2 kinds of bindings (didn't get the details).

### Actions

All the deferred actions get put here.

### Render and AfterRender

Here's where the DOM is manipulated.

The afterRender queue is where you schedule activities after Ember has manipulated the DOM.

### Destroy

Where objects are destroyed.

## Why does Backburner exist?

* Performance
* Modularity
* Cleaner code
* Better debugging
* Sharing the wealth

Erik asserts that the source code for Backburner is very readable.

Debugging deferred / asynchronous actions is hard.

But Backburner makes this much easier.

New York Ember meeting talks about Ember testing.


