---
layout: default
title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

# Welcome

This is my personal blog.

# Insert title here

Here is some text

## This is a subsection

- it can have many points
- which look like this

# This section will host an image!

Image can be seen here: 


# testing site map

<div class="button-grid">
  <a href="/02-01-2026_first_post.html" class="btn">My First Post</a>
  <a href="/2026/01/05/second-post.html" class="btn">Second Post</a>
  <a href="/about.html" class="btn">About</a>
</div>

# auto test
<div class="button-grid">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="btn">
      {{ post.title }}
    </a>
  {% endfor %}
</div>
