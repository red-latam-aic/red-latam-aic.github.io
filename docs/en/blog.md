---
layout: default
title: Blog
lang: en
ref: blog
permalink: /en/blog/
---

# Blog

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'en'" %}
{% for post in posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})** — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
