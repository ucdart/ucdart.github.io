---
layout: default
title: News
published: true
---
<section>
	<h3>{{ page.title }}</h3>
	<ul>

	  {% for post in site.posts %}
	    <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
	  {% endfor %}
	</ul>
</section>
