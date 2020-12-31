---
layout: page
title: Site Credits
---


![black and white windmill - AK Blog Credits](/assets/img/bnw-windmill.jpg)

_Photo by <a href="https://stocksnap.io/author/ianlivesey">Ian Livesey</a> from <a href="https://stocksnap.io">StockSnap</a>_


#### The Basics

- Github, Jekyll, Poole


#### Resources

- Start with the [Poole](https://github.com/poole/poole) for setting up a basic site. When in doubt, you may refere to the Jekyll and Github Pages documentation:


	- The official [Jekyll](http://jekyllrb.com/) website.

	- Github Pages [documentation](https://help.github.com/articles/using-jekyll-with-pages/) with Jekyll.


- [@joshualande](http://twitter.com/joshualande) blog article on using [Jekyll, Github Pages, and Poole](http://joshualande.com/jekyll-github-pages-poole) provided all the required details about setting up blog "pages", the blog posts archive page, adding disqus comments etc. **Highly recommend** this article.

- TODO: Fulltext Search on Jekyll site <http://dreamand.me/web/fulltext-search-at-jekyll-site/>

- TODO: Add tags and categories for posts; list posts under archives by tags/categories.
Is this what I should look at? <https://github.com/jekyll/jekyll-archives>

#### Inspiration

The inspiration to do a blog on github pages came to me while I was exploring markdown. As of Dec 2015, I get inspired by a very informative blog by [Ben Balter](https://github.com/benbalter/benbalter.github.com) that uses Jekyll + Github Pages. 


#### Tips

There are some gotchas that one has to be aware of when setting up the site. I had trouble with `baseurl` config setting when _not_ using custom domain. Came across a Jekyll issue [comment](https://github.com/jekyll/jekyll/issues/332#issuecomment-18952908) on how to serve on localhost. The following should allow the render on localhost without affecting the relative URLs of the posts:
	
  `$ jekyll serve --baseurl '' `

If you want to serve 'drafts' on localhost, then you may try the following:
	
  `$ jekyll serve --drafts server --baseurl ''`
	
