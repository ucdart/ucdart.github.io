---
layout: default
title: Publications
published: true
---

### Publication
[Bibtex](/utilities/dart_pub.bib) of DART lab publications. 

#### Journal

{% assign papers = (site.publication | sort: 'sort_key', 'first') %}
<ol>
	{% for paper in papers %}
	{% if paper.type =="article" %}	
	<li> 
    {% if paper.note !=null %} 
    	<b>({{ paper.note }})</b> 
    {% endif %} 
    &nbsp; {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span>," <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a></li>
	{% endif %}	
	{% endfor %}
</ol>

#### Conference

<ol>
	{% for paper in papers %}
	{% if paper.type =="conference" %}	
	<li>{{ paper.author }}, <b>"{{ paper.title }},"</b> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}	
	{% endfor %}
</ol>