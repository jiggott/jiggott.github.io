---
layout: page
title: All blog posts
permalink: /blog/
---

{% for post in site.posts %}
<p><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a> <small>({{ post.date | date: "%-d %b %Y" }})</small> {% assign tags = post.tags %}{% for tag in tags %}<span class="tag">{{ tag }}</span> {% endfor %}</p>
{% endfor %}