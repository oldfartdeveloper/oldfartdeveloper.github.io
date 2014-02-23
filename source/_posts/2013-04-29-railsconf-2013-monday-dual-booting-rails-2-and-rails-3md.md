---
layout: post
title: "Dual Booting Rails 2 and Rails 3"
description: "Dual Booting Rails 2 and Rails 3"
category: Presentation
tags: ['RailsConf 2013']
---

## Summary

* You *can* dual boot Rails 2 and Rails 3

<!-- more -->

### Pros

* One of the most valuable sessions for me, in that we have "gone to the wall" to do a conversion,
  and we fail miserably because we run out of time and have to "retreat".  Very demoralizing.

### Cons

* But what are the steps?  Fortunately, this was covered in a
  [later session](/blog/railsconf2013/Thursday/UpgradingLongLivedRailsTo4.md) by someone else.

## Raw

### History/Reasons

Numbers...

Upgrading to Rails 3

1. Procrastinate vs.
1. Goals

Have to make some decisions:

* Putting it off
* Rearchitecting the app first
* Do it all in a big spike.2
* Have a ruby19 branch.

Reasons to move forward:

* Rails 3? Why now?
* Someone will make upgrading easier soon!
* Oh man, this is going to be awful.

But, here's what we want:

1.  burke/zeus
1.  recruiting people to work on Rails 2.x is really uphill now
1.  security fixes.

Finally, they were finding it was more expensive to stay on Rails 2 than it was to upgrade to Rails 3.

*New Relic took 2 months to do it.*

### Rules

Don't break the world.

* Can't bring down production.
* Keep everyone (i.e. other developers) happy.  Don't make them miss deadlines.
* Keep ourselves happy

### How They Did It

**Most Memorable Technique: Keep everything in the master branch and use environment variable to switch
between Rails 2 and Rails 3.**  In this way, you don't have the constant merging.

They used rails/rails_upgrade

Spent a lot of time in bundler

In Gemfile

platforms :ruby_18 do
  gem 'debugger'
end

platforms :ruby_19 do
  gem 'ruby-debug'
end

Monkey patched Bundler so that they could have two Gemfile.lock files

So, now they could do incremental improvements:

$ script/server

$ script/server3

Now they could to go master.

Now they could merge into upstream, but the Rails 3 was installed in production.

So, use environment variable to change config.rb to either load bundler (3) or rails(2)

In config/application.rb

def self.rails3_config(config)

...

def self.rails2_config(config)


Have tests you trust.

Jenkins

Created a Rails 3 job.  They could convert the Rails 2 test into Rails 3.

Branch by abstraction: a pattern for making large scale

Disable deprecation warnings.

Routes still work.
Od mailers still work.
Old models can still work.

Helpers - All helpers are included by default.

Error handling - watch for Rails 3 moving error handling moving to middleware.

Rollout:

We want you to test in Rails 3.
Make everyone a tester.
A couple of days before production, all submits went to Rails 3.

Rails 2 and Rails 3 are incompatible sessions.

envato / rails_4_session_flash_backport

Pause the world on the day you deploy.

Minor breakages:

* Breaking the audi trail.  Lost track of who changed.  Caused by obsolete 3rd-party gem.  Moral: unexpected things
will happen.
* ActiveScaffold - moved from Protytpe to Jquery.
* Lost BackgroundJob instrumentation.

Finally tagging green build off of Rails 2 tests.

Afterwards, cleaning up all the code.

## Lessons learned

1.  Be aware that you have potential to hurt other develoeprs
1.  Deprecate ActiveScaffold
1.  Allocate sufficient resources for cleanup after deployment.
1.  Jenins jobs for both rails versions was invaluable.

## Place to get libraries that they used that might be useful for us:
newrelic.com/rails3_upgrade


Use Resque.

