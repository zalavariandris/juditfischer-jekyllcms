---
title: news
layout: default
exclude: true
---

{% for post in site.posts %}
<div class="surface">
<figure>
	<img width="100px" src="{{post.feature_image}}">
</figure>
<h3>
	<a href="{{ post.url }}">
		{{ post.title }}
	</a>
</h3>
<time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
{{ post.excerpt }}
</div>
{% endfor %}