---
layout: default
title: "my-blog"
---

<p>Read the latest articles below:</p>

<div class="blog-list">
{% for post in site.posts %}
    <div class="blog-item">
        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt }}</p>
        <p>{{ post.author }}</p>
        <a class="read-more" href="{{ site.baseurl }}{{ post.url }}">Read More</a>
    </div>
{% endfor %}
</div>
