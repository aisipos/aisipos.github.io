---
layout: page
title: Blog
tagline: Challenging the status quo of Software Engineering
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<h1>{{ site.posts[0].title }}</h1>
{{ site.posts[0].content }}


