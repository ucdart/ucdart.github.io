---
layout: default
title: Davis Advanced RF Technology
published: true
use_math: true
---

Test a display math with equation number:
\begin{equation}
   |\psi_1\rangle = a|0\rangle + b|1\rangle
\end{equation}
Is it O.K.?

Test a display math with equation number:
$$
  \begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
  \end{align}
$$
Is it O.K.?

Test a display math with equation number:
\begin{align}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align}
Is it O.K.?

And test a display math without equaltion number:
\begin{align\*}
    |\psi_1\rangle &= a|0\rangle + b|1\rangle \\\\
    |\psi_2\rangle &= c|0\rangle + d|1\rangle
\end{align\*}
Is it O.K.?



<p class>
{% for post in site.blog limit:6 %}
      » [{{ post.date | date_to_string }}] » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a><br>
{% endfor %}
</p>

![test image test](image/tunable-filter.jpg)

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
