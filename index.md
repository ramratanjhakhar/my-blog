---
layout: default
title: "Home"
---

<h1>Welcome to My Blog</h1>
<p>Read the latest articles below:</p>

<div class="blog-list">
{% for post in site.posts %}
    <div class="blog-item">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <p class="date">{{ post.date | date: "%B %d, %Y" }}</p>
        <p>{{ post.excerpt }}</p>
        <a class="read-more" href="{{ post.url }}">Read More →</a>
    </div>
{% endfor %}
</div>
