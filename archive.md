---
layout: page
title: Archive
---

<p class="message">
 Let us change our traditional attitude to the construction of programs: Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to humans what we want the computer to do. -- Donald E. Knuth, Literate Programming, 1984
</p>

**A list of articles from the Archive...**

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
### {{ year.name }}

{% for post in year.items %}
  * {{ post.date | date_to_string: "ordinal", "US" }} &raquo; [ {{ post.title }} ]({{site.baseurl}}{{ post.url }})
{% endfor %}

{% endfor %}


<br/>

*Articles by <a href="{{ site.baseurl }}/categories/">categories</a>*