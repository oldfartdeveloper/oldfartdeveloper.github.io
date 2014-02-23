---
layout: post
title: "Natural Languages"
description: "Natural Languages"
category: Presentation
tags: ['RailsConf 2013']
---

## Summary

* Natural Languages is the programming effort to understand natural languages (like *English*)
  so that software can help interpret information contained in the vast expanses of natural language
  expressions on the web.

<!-- more -->

### Pros

* Good top-down view

### Cons

* Sad to see that Ruby is not in the front vanguard in this effort.

## Raw

What is Natural Language Processing?

* What is it?
* Why is it so Difficult?
* Why is it important?

### Definition:

Analyzing, understanding and generating the language that humans use to interface with computers.

* Spell Checking
* Predictive Text
* Auto Summarization
* Content categorization
* Machine Translation

Includes things like OCR which are huge efforts in themselves.

Example: "Buffalo buffalo Buffalo buffalo buffalo buffalo Buffalo buffalo."

No perfect solution exists

* Experts disagree
* Fixing one piece frequently breaks others.
* Language itself is a moving target.
    * Different cultures, grammar, syntax
    * Language is constantly evolving
    * Technological advances influence language.
* Mobile devices
* Many aspects are computationally complex
* Today vs. 10 years ago
* Hardware has advanced

## Why is it Important?

* 43% of employee's time spent in information hunting.
* Demand/need is increasing steeply.
* Everyone has a "big data" problem.

## 3 Common Approaches

* rule-Based Analysis
* statistical analysis
* Machine learning

## Basic Building Blocks

* POS Tagging
* Chunking
* Sentence Detection
* Word stemming
* Tokenizing
* Work Relationships
* Co-Reference Resolution
* Named-Entity Recognition

## Tools & Libraries

* NLP Toolkit (Python)
    * Leading NLP Toolkit/Framework
    * Strong support from the academic world (SciPy, NumPy)
    * Python was chosen for its expressiveness, ease-of-use
* Ruby, not much
    * Chronic
    * Linguistics
    * Punkt Segmenter
    * Ruby Stemmer (unmaintained)
    * Treat (The Ruby NLP toolkit)
        * Extraction
        * Chunking
        * Sentence Segmentation
        * Stemming
        * Machine Learning
        * Inflection
        * Serialization
* What happens when you need more?
    * JRuby
    * Leverage well-established, mature Jana libraries.
