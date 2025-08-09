---
layout: default
title: Blog
---
<link rel="stylesheet" href="/assets/style.css">

# Blog

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <small>— {{ post.date | date: "%b %d, %Y" }}</small>
  </li>
{% endfor %}
</ul>