---
layout: post
title: "C Ruby"
description: "Why Working With Ruby and C Together Is Great"
category: Presentation
tags: [LA RubyConf 2014]
---

Summary: getting to know how **C** is used in **Ruby** and the synergies between them:

* Understanding Ruby
* Speeding up Ruby
* Accessing non-Ruby libraries.

<!-- more -->

Details follow:

### Understand Ruby

Some things you can only find out from reading the C code.

### Speed Up Ruby

* Rewrite parts of your code in C
* 20x-50x speed gain.

### C Extensions

#### Ruby + C

Best of both worlds

### Level 1 -- build Ruby from scratch

ruby-2.0.0-p247 is stable

Configure (Mac)

```bash
$ brew install openssl
$ autoconf
$ ./configure --prefix= $HOME/myruby --with--opot-dir=/usr/l...
```
creates lots of output.

compile and Build

```
$ make
```

Then check it

```
$ make check
```

Then install it

```
$ make install
```

Setup PATHSs

1.  Include your new ruby in `$PATH`.
...

Verify

```
$ which ruby
```
...

gem env

Can check further by installing Rails

Can even set up in RubyMine

### Level 2 - Debugger

lldb - he showed how to use this debugger to see how you walk in C.

Can use XCode lldb

#### Folder Structure

`ext` and the root folder are the most interesting.

### Level 4 - Hacking

### Epilog

* ruby internals
* ruby metaprogramming
* ruby object model

and the rest I didn't get.
