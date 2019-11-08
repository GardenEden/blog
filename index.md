---
layout: page
title: 技术收集
---
## 近期

{% for post in site.posts limit:5 %}

- [{{ post.title }}]({{ post.url }}), *{{ post.date | date: "%Y-%m-%d" }}*

{% if post.description %}

  > {{ post.description }}

{% endif %}

{% endfor %}

- [更多…](/archive)

{% for tag in site.index.showtag %}

## {{ tag }}

{% for post in site.tags[tag] %}

- [{{ post.title }}]({{ post.url }})

{% if post.description %}

  > {{ post.description }}

{% endif %}

{% endfor %}

{% endfor %}
