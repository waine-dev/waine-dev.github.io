---
layout: default
title: 博客
---

# 博客文章

{% for post in site.posts %}
<article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">{{ post.date | date: "%Y年%m月%d日" }}</p>
    {% if post.excerpt %}
    <p>{{ post.excerpt }}</p>
    {% endif %}
</article>
{% endfor %}

