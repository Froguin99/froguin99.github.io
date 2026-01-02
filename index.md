---
layout: default
title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

# Welcome

if you've stumbled across this, welcome. I'm not quite sure what this'll end up being but as of writing I like the idea of keeping some form of blog, not with the aim of sharing to the world, rather with the aim of letting those who are interested in whatever is going on here find something to look at for 5 minutes before promptly moving on. It will also act as a test for my (poor!) coding skills in my spare time. 


## This is a subsection

- it can have many points
- which look like this



<h1>Latest Posts</h1>

<div class="posts-feed">
  {% for post in site.posts %}
    <article class="post-card">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%d %b %Y" }}</p>
      <div class="post-content">
        {% assign parts = post.content | markdownify | split: '</p>' %}
        {% assign count = 0 %}
        {% for part in parts %}
            {% assign part = part | strip %}
            {% if part != '' %}
            {{ part }}</p>
            {% assign count = count | plus: 1 %}
            {% if count == 2 %}
                {% break %}
            {% endif %}
            {% endif %}
        {% endfor %}
        </div>
        <a href="{{ post.url | relative_url }}" class="read-more">Read more</a>
      <hr>
    </article>
  {% endfor %}
</div>


# Site map

<div class="button-grid">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="btn">
      {{ post.title }}
    </a>
  {% endfor %}
</div>
