---
layout: default
title: Publications
published: true
---

[Bibtex](/utilities/dart_pub.bib) of DART lab publications. 

### Journal

{% assign papers = (site.publication | sort: 'sort_key') %}
<ol>
	{% for paper in papers reversed %}
	{% if paper.type =="article" %}	
	<li>     
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
    {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> </li>
	{% endif %}	
	{% endfor %}
</ol>

### Conference

<ol>
	{% for paper in papers reversed %}
	{% if paper.type =="conference" %}	
	<li> 
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
     {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }},"</span> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> </li>
	{% endif %}	
	{% endfor %}
</ol>