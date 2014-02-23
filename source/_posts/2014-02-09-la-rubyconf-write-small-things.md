---
layout: post
title: "Writing Small Things"
description: "Using Refactoring Techniques to Improve Code and Maintainability"
category: Presentation
tags: [LA RubyConf 2014]
---

## Small Code

* Not about less code.
* Rather it's about organizing the code into smaller classes and smaller methods.
* Don't start with it; refactor towards it.

Why?

<!-- more -->

* We don't know the future
* Raise the level of abstraction
* Create composable components
* Prefer delegation over inheritance.

all so you can enable future change.

Challenges of small code:

* Dependency Management
* Context Management

Main Tools

* extract method
* extract class
* composed method

Screensize is good size constraint.

Minimize number of arguments.

# Methods

"The object programs that live best and longest are those with short methods."

-Refactoring by Fields, Harvey, Fowler, Black

## The first rule of methods

Do one thing.  Do it well.  Do only that thing. (don't have side effects)

Use descriptive Names

The fewer arguments, the better.  (constructor can take option hash)

Separate Queries from Commands

Don't repeat yourself.

## let's Build aCommand Line Option Library

How do we isolate abstractions?

* Separate the "what" from the "how"

# Miscellaneous

presentation will be available on his SlideShare account soon.

# Presenter

Mark runs Enable Labs, consulting

Mark Menard

@mark_menard

Ruby for about 5 years

'The great thing about writing shitty code that "just works," is that it is too risky and too expensive to change,
so it just lives forever.'
