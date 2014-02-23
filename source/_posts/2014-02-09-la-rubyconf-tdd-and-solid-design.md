---
layout: post
title: "TDD and SOLID Design"
description: "A SOLID understanding can improve not only your code but your TDD"
category: Presentation
tags: [LA RubyConf 2014]
---

Intention of SOLID principle is to make better code and more testable code.  Here's how.

<!-- more -->

## Wishful Testing

In a shipping class example,

```ruby
Shipping::Rate.stub(:new).with(
order.stub(non_digital_items).and_return(0)
```

Now these can be wrapped by methods.

## Liskoff Substitution Principle

Derived classes must be substitutable for their base classes

Contract Test

```ruby
it_should_behave_like "s shipping method"
```
* Dependency inversion
* Open Closed
* Interface Segregation

## Summary

> "I'm not a great programmer; I'm just a good programmer with great habits"  --Kent Beck

SOLID principles help you acquire great habits. @sebasoga

Question: Any of these principles good for testing ActiveRecord models?

Answer: Only have your model info specific to database (scopes, etc).
Business logic put into different classes.
