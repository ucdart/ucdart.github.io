---
layout: default
title: Publications
published: true
---

<!-- [Bibtex file](/utilities/dart_pub.bib) of DART lab publications. -->

<!--
<div class="alert alert-success">
    <strong>Four papers</strong> accepted to <a href="http://ims2017.org/">IMS2017</a>!
</div>
-->

[Journals](#journals)   |    [Conferences](#conferences)    |     [Patents](#patents)

### Journals

{% assign papers = site.publication | sort: 'sort_key' %}
<ol reversed>
	{% for paper in papers reversed %}
		{% if paper.type =="article" %}
		<li>     
    		{% if paper.note != null %}
				<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
			{% endif %}
    		{{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf" target = "_blank"> <img src = "/images/oa-icon.png"> </a> </li>
		{% endif %}
	{% endfor %}
</ol>

### Conferences

<ol reversed>
	{% for paper in papers reversed %}
	{% if paper.type =="conference" %}
	<li>
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
     {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }},"</span> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf"  target = "_blank"> <img src = "/images/oa-icon.png"> </a> </li>
	{% endif %}
	{% endfor %}
</ol>

### Patents

<ol reversed>
	{% for paper in papers reversed %}
	{% if paper.type =="patent" %}
	<li>
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
     {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }},"</span> US Patent # {{ paper.patent }}, {{ paper.month }}, {{ paper.year }}. </li>
	{% endif %}
	{% endfor %}
</ol>
