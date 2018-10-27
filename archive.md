---
layout: page
title: Archive
---

<p class="message">
 Let us change our traditional attitude to the construction of programs: Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to humans what we want the computer to do. -- Donald E. Knuth, Literate Programming, 1984
</p>

A list of articles from the Arhives...

{% for post in site.posts %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{site.baseurl}}{{ post.url }})
{% endfor %}
