---
layout: post
title:  "Problems Solved"
date:   2021-11-21
categories: problems jekyll
tags: featured
image: /assets/article_images/2014-08-29-welcome-to-jekyll/desktop.JPG
---

## Jekyll

### Webrick Error on Jekyll Serve

When I first attempted to build and serve this site, the system threw an error related to "webrick":

bundler: failed to load command: jekyll (/usr/local/lib/ruby/gems/3.0.0/bin/jekyll)
/usr/local/lib/ruby/gems/3.0.0/gems/jekyll-3.9.0/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)

 The problem is that Ruby 3.0 does not come with webrick. Webrick is the Ruby module that provides http server functionality. Fortunately, there is a simple solution:

`bundle add webrick`

That fixed it!