---
layout: page
title: Site Credits
---



#### The Basics:

- Github
- Jekyll
- Poole


#### Resources:

- Start with the [poole](https://github.com/poole/poole) for setting up a basic site. When in doubt, you may refere to the Jekyll and Github Pages documentation:


	- The official [Jekyll](http://jekyllrb.com/) website.

	- Github Pages [documentation](https://help.github.com/articles/using-jekyll-with-pages/) with Jekyll.


- [@joshualande](http://twitter.com/joshualande) blog article on using [Jekyll, Github Pages, and Poole](http://joshualande.com/jekyll-github-pages-poole/) provided all the required details about setting up blog "pages", the blog posts archive page, adding disqus comments etc. **Highly recommend** this article.

- TODO: Fulltext Search on Jekyll site <http://dreamand.me/web/fulltext-search-at-jekyll-site/>

- TODO: Add tags and categories for posts; list posts under archives by tags/categories.
Is this what I should look at? <https://github.com/jekyll/jekyll-archives>

#### TIPS:

- There are some gotchas that one has to be aware of when setting up the site. I had trouble with `baseurl` config setting when _not_ using custom domain. Came across a Jekyll issue [comment](https://github.com/jekyll/jekyll/issues/332#issuecomment-18952908) on how to serve on localhost. The following should take care of the localhost start:
	-	`jekyll serve --baseurl '' `
	