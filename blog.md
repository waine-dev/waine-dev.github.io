---
layout: page
title: 博客
permalink: /blog/
---

# 博客文章

{%- if site.posts.size > 0 -%}
  <ul class="post-list">
    {%- for post in site.posts -%}
    <li>
      {%- assign date_format = site.minima.date_format | default: "%Y年%m月%d日" -%}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      {%- if post.excerpt -%}
        <div class="post-excerpt">
          {{ post.excerpt }}
        </div>
      {%- endif -%}
      {%- if post.categories.size > 0 -%}
        <div class="post-categories">
          <span>分类: </span>
          {%- for category in post.categories -%}
            <span class="category-tag">{{ category }}</span>
          {%- endfor -%}
        </div>
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>
{%- else -%}
  <p>暂无文章发布。</p>
{%- endif -%}

