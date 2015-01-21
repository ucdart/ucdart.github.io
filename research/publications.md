---
layout: default
title: Publications
published: true
---

### Publication
[Bibtex](/utilities/dart_pub.bib) of DART lab publications. 

#### Journal

{% assign papers = (site.publication | sort: 'sort_key', 'last') %}
<ol>
	{% for paper in papers %}
	{% if paper.type =="article" %}	
	<li> <b>{{ paper.note }}</b> &nbsp; {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a></li>
	{% endif %}	
	{% endfor %}
</ol>

#### Conference

<ol>
	{% for paper in papers %}
	{% if paper.type =="conference" %}	
	<li> <span style='font-weight:600;color=red;'>{{ paper.note }}</span> &nbsp; {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }},"</span> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> </li>
	{% endif %}	
	{% endfor %}
</ol>