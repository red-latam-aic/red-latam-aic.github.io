---
layout: default
title: Blog
lang: pt
ref: blog
permalink: /pt/blog/
---

# Blog

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'en'" %}
{% for post in posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
