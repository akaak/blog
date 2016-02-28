---
layout: post
title: New Static Site Generator (Lektor)
---

There are many static site generators. The new open source static site generator is Lektor. Armin Ronacher (the creator of Python Flask framework) came up with this static site generator in December 2015. Armin wrote a blog [post](https://www.getlektor.com/blog/2015/12/hello-lektor/) introducing this Lektor project and the why he created this project.

It looks really powerful and the fact that it is built on Python gave me a reason to try it.

Project website: <https://www.getlektor.com> and on [github](https://github.com/lektor/lektor)


__What is Lektor?__

> A flexible and powerful static content management system for building complex and beautiful websites out of flat files — for people who do not want to make a compromise between a CMS and a static blog engine.

> Getting your ideas implemented is as easy as making breakfast eggs.

## Installation

Running the following command from the command line installs Lektor:

```
$ curl -sf https://www.getlektor.com/install.sh | sh
```

**Command output within in the terminal**



    Stored in directory: /Users/ak/Library/Caches/pip/wheels/c7/28/31/bac6d0b118c0bdcbf57f9219afdf2e624379c07efa6c769dbc
    Successfully built Flask watchdog itsdangerous PyYAML argh pathtools MarkupSafe ndg-httpsclient enum34 pycparser
    Installing collected packages: pytz, Babel, Werkzeug, MarkupSafe, Jinja2, itsdangerous, Flask, inifile, mistune, click, EXIFRead, PyYAML, argh, pathtools, watchdog, six, enum34, ipaddress, pyasn1, idna, pycparser, cffi, cryptography, pyOpenSSL, ndg-httpsclient, requests, Lektor
    Successfully installed Babel-2.2.0 EXIFRead-2.1.2 Flask-0.10.1 Jinja2-2.8 Lektor-1.2.1 MarkupSafe-0.23 PyYAML-3.11 Werkzeug-0.11.4 argh-0.26.1 cffi-1.5.2 click-6.2 cryptography-1.2.2 enum34-1.1.2 idna-2.0 inifile-0.3 ipaddress-1.0.16 itsdangerous-0.24 mistune-0.7.1 ndg-httpsclient-0.4.0 pathtools-0.1.2 pyOpenSSL-0.15.1 pyasn1-0.1.9 pycparser-2.14 pytz-2015.7 requests-2.9.1 six-1.10.0 watchdog-0.8.3

    All done!



### After the Installation

Once Lektor is installed, you may run the `which lektor` command and `lektor` is found.


    AK-Mac:getlektor ak$ which lektor
    lektor is /usr/local/bin/lektor
    AK-Mac:getlektor ak$ 


### Creating a Project

Run the following command to start a project.
`$ lektor quickstart`

Once a project is started, Lektor creates necessary folders and files.

### Starting the Site

`$ lektor server`

shows...


    AK-Mac:marketing_site ak$ lektor server
     * Project path: /Users/ak/dev/getlektor/marketing_site/Marketing Site.lektorproject
      * Output path: /Users/ak/Library/Caches/Lektor/builds/6ee3d70343f67651db511f4c62b9ddde
       * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
       Started source info update
       Finished source info update in 0.03 sec
       Started build
       U index.html
       U about/index.html
       U projects/index.html
       U blog/index.html
       U static/style.css
       U blog/first-post/index.html
       Finished build in 0.08 sec
       Started prune
       Finished prune in 0.00 sec

Go to the local host at http://127.0.0.1:5000/ to browse the site!

![Lektor Site on Localhost]({{site.baseurl}}/assets/img/lektor1.png)


### Building the Site

`$ lektor build`

builds and keeps the whole site content in a Cache. As mentioned in the documentation, you may find out the built files location using `$ lektor project-info --output-path` command.

If I go to my local cache the site files look like below:


    AK-Mac:6ee3d70343f67651db511f4c62b9ddde ak$ tree .
    .
    ├── about
    │   └── index.html
    ├── blog
    │   ├── first-post
    │   │   └── index.html
    │   └── index.html
    ├── credits
    │   └── index.html
    ├── index.html
    ├── projects
    │   └── index.html
    └── static
        └── style.css

    6 directories, 7 files

    AK-Mac:6ee3d70343f67651db511f4c62b9ddde ak$ pwd
    /Users/ak/Library/Caches/Lektor/builds/6ee3d70343f67651db511f4c62b9ddde
    AK-Mac:6ee3d70343f67651db511f4c62b9ddde ak$ 


### Deploy Your Site

Once you are satisfied with the Site files/content, you may deploy the site to a platform of your choice.


### In Closing
It cannot be easier than this to get started with a static site.
Big Thanks to [@mitsuhiko](http://twitter.com/mitsuhiko).

