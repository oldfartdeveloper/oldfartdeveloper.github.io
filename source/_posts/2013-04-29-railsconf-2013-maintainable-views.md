---
layout: post
title: "Maintainable Views"
description: "Maintainable Views"
category: Presentation
tags: ['RailsConf 2013']
---

## Summary

* Some suggestions for doing good software practices in view templates

<!-- more -->

### Pros

* Contrasted conflicting needs of designers vs programmers.
* Good discussion of helpers vs partials vs presenters and where to use each.

### Cons

* Can't think of any

## Raw

Assumption: already know how to write markup.

Unmaintainable templates

* Markup repetition
* Logic in templates

Markup Repetition

* Good designer repeat tehmselves.
* Good programmers don't.

Avoid markup repetition

* Abstract interface components.
* Use partials.

Logic in templates

* Highly repetitive.
* Painful to test.

## Problems with Helpers

* Big projects end up with *tons*.
* Difficult to organize.
* Complex logic isn't well suited for them.
* Don't *feel* right.

What presenter wants is decorator pattern.

* wraps a single object
* Transparent interface
* forwards methods to originla object

In our case:

* Adds presentational logic to models without affecting the model itself.

Implementing a Decorator.

* Uses a +method_missing* to forward object.
* He has a base decorator class.
* Whatever is used for a model goes into a single Decorator subclass for that model.
* In the view, the decorator looks like the original model object.

Draper

* Access to the view context
* Easily decorate collections
* Prtends to be decorated object (helpful for +form_for+ and such)
* Easily decorate associations

Complex views

Unique and/or complex UI behavior will quickly outgrow helpers

Uses Presentation Model

The Presentation Model is of a self-contained class that represents all the data and behivor of the UIT window.

Learning from JavaScript libraries

* Thanks, Backbone.

So, presenter is passed

* template
* each model object needed.

a ```#to_s``` method renders.

Presenter likes to use a helper to create the presenter/view objects.

This concept comes built-in with Rails. ```form_for``` which you can create a custom ```FormBuilder``` class.

Final tips

* Use i18n
* Find gems to do this work for you (eg. simple_form, table_cloth)

New project called ```self``` that is trying to solve a lot of these concerns.
