---
layout: default
title: UCDart/Research
---



### Publication

<ol>
	{% for paper in site.publication %}
		<li><span>{{ paper.author }}, {{ paper.title }} <i> {{ paper.journal }}</i>, {{ paper.month }}, {{ paper.year }}.  </span></li>
	{% endfor %}
</ol>
