---
layout: post
title: Not so Static Web Sites
---

Static websites using HTML and CSS may setup with little or no effort. If you, however, need to make any changes to these websites then it is not always easy. Particularly, if you are trying to change something in the header or footer that is on all the pages of this static (HTML only) website or web pages.

By having some server side scripting you can make a website behave dynamic. Using Python as the platform there are a couple of options. Flask project based on Python, offers simple website management, url protection, and Jinja templates (you can use other templates with Flask as well).

The following github project provides a complete flask + ninja website using the server side includes giving a dynamic website with very little effort:

<https://github.com/mjhea0/thinkful-mentor/tree/master/python/jinja>

Alternatively, you could use a static site generator approach for setting/updating/publishing a static website. [StaticGen](https://www.staticgen.com) is a website just dedicated for top open-source static site generators.  

Some popular static site generator platforms are:

- jekyll (used by github pages; ruby based)
- pelican (python based)
- hyde (python based)
- sphinx (the best for document generation)
- mkdocs (python based)
- bonsai (ruby based?)

Most of these frameworks support markdown and/or restructured text. Using some of these tools/frameworks you can easily get started with a very dynamic website.

One important point to note is that these frameworks do NOT offer an easy way to edit/add pages without some kind of developer background. These tools would definitely not give a rich user interface and tools of a full blown content management system (CMS) such as wordpress or drupal.

So, if you are looking for creating, editing and automatically publishing an almost static website that can be supported by a designer/developer then Flask + Jinja is the way to go! 


