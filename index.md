---
layout: default
title: "my-blog"
---
<h2>Latest Articles</h2>

<div class="post-list">
    {% for post in site.posts %}
    <div class="post-preview">
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <div class="post-meta">
            <span>By {{ post.author }}</span> | 
            <span>{{ post.date | date: "%B %d, %Y" }}</span>
        </div>
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
    </div>
    {% endfor %}
</div>
