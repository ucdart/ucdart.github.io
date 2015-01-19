---
layout: default
title: UCDart/Research
---



### Publication

#### Journal

<ol>
	{% for paper in site.publication %}
	{% if paper.type =="article" %}	
	<li>{{ paper.author }}, "{{ paper.title }}," <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}	
	{% endfor %}
</ol>

#### Conference

<ol>
	{% for paper in site.publication %}
	{% if paper.type =="conference" %}	
	<li>{{ paper.author }}, "{{ paper.title }}," <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}	
	{% endfor %}
</ol>
