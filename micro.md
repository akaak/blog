---
layout: page
title: Micro
permalink: /micro
---

<p class="message">
<em>Short posts, links, thoughts, and notes that don't need a full article.</em>
</p>

{% assign micro_posts = site.micro | sort: 'date' | reverse %}
{% assign micro_by_month = micro_posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}

<nav class="micro-month-nav">
{% for group in micro_by_month %}
  {% assign month_id = group.items.first.date | date: '%Y-%m' %}
  {% assign month_label = group.items.first.date | date: '%b-%Y' | upcase %}
  <a href="#month-{{ month_id }}">{{ month_label }}</a>{% unless forloop.last %} &nbsp;&middot;&nbsp; {% endunless %}
{% endfor %}
</nav>

<div class="posts">
{% for group in micro_by_month %}
  {% assign month_id = group.items.first.date | date: '%Y-%m' %}
  <h2 class="micro-month-heading" id="month-{{ month_id }}">{{ group.name }}</h2>
  {% for post in group.items %}
  <article class="post micro-post">
    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">{{ post.date | date_to_string: "ordinal", "US" }}</time>

    {{ post.content }}
  </article>
  {% endfor %}
{% endfor %}
</div>
