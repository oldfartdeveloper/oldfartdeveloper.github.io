---
layout: post
title: "DHH Keynote"
description: "DHH Keynote"
category: Presentation
tags: ['RailsConf 2013']
---
## Summary

* DHH stays consistent: Rails purpose is to be a big tent but not everything for all people.
* Web is about HTML.  Other frameworks fall away (Silverlight, Flash)
* Quote from Joel on Software: "Good Software Takes Ten Years.

<!-- more -->

Rest of talk covered the *BaseCamp* way of doing things, mainly to speed up dynamic HTML generation:

* Key-based cache expiration (generational caching).
* Russian Doll nested caching.
* Use of Javascript sparingly to handle local issues like timezone.

### Pros

* Liked how he put HTML processing as the purpose of Rails.

### Cons

* Neglected to mention that BaseCamp now has nearly a megabyte of Javascript.
* More subdued presentation; I enjoy the fire/brimstone more.

## Raw

Good frameworks are extractions, not inventions.

Rails started in 2003 (10 Years)

2003: 512MB costs $49
2013: 8GB costs $29

Other communities value stability.

Ruby/Rails community willing to sacrifice for progress.  Pioneer spirit.

Rails 2.3 / 2009 is the halfway.

"Good Software Takes Ten years.  Get Used To It" - Joel on Software, 2001

Purpose: big tent, but not be everything for all people.

Context: Dynamic Hypertext documents

the HyperText Markup Lanuage is more than just a delivery mechanism.

Rails purpose is to support web documents and things that "feel like documents."  This is the part of IT that DHH is
interested in.

Constraints are liberating.

Silverlight, Flash dissed HTML.  DHH maintains that HTML is the inspiration.

iOS is more interesting but is still mostly used for games (according to DHH).

So, newest Basecamp embraces the document.  Evolve the document so that it's a worthy competitor to the
GUI-approaches.  Faster.  So can we get the speed without changing the underlying HTML patterns?

To make things faster:

* Key-based cache expiration (generational caching).
* Russian Doll nested caching

But, what about time zones?

Use Javascript to take care of this.

Some things then can do Turbolinks

Finally: Polling for JavaScript updates.

RJS used.
