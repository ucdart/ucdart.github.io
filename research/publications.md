---
layout: default
title: Publications
---
### Publication

#### Journal

<ol>
	{% for paper in site.publication %}
	{% if paper.type =="article" %}	
	<li>{{ paper.author }}, <b>"{{ paper.title }},"</b> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}	
	{% endfor %}
</ol>

#### Conference

<ol>
	{% for paper in site.publication %}
	{% if paper.type =="conference" %}	
	<li>{{ paper.author }}, <b>"{{ paper.title }},"</b> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}	
	{% endfor %}
</ol>
