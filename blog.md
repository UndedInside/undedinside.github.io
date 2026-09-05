---
layout: page
title: Blog
permalink: /blog/
---

<ul>
  {% for post in site.posts %}
    <li>
      <b><a href="{{ post.url}}">({{ post.date | date: "%Y-%m-%d" }}) {{ post.title }}</a></b><br>
      {{ post.hook }}
      <p></p>
    </li>
  {% endfor %}
</ul>
