<p> Due to its low insertion loss, high isolation, high linearity, wide bandwidth, and near-zero dc power consumption, radio frequency micro-electromechanical (RF-MEMS) switches have been an emerging technology with significant potential in many high frequency circuits and systems, especially those requiring reconfiguration. Compared to other high frequency switching technologies, metal contact RF-MEMS switches have the highest figure of merit (FoM, defined as 1/R<sub>on</sub>C<sub>off</sub>) because of its ultimately low contact resistance and off-state capacitance. In addition, metal contact RF-MEMS switches have extremely large bandwidth that can extend from dc to beyond 100 GHz. </p>

<p> However, the reliability issues associated with RF-MEMS contact switches have been a major barrier for the wider adoption of the technology. Significant efforts have been devoted to improving the lifetime (primarily in terms of cycling time) of RF-MEMS contact switches. For example, the Radant MEMS switch can be cycled up to 100 billion times under cold-switching conditions. Under hot-switching conditions, however, the reliability of these switches degrades quickly with a sharp increase in contact resistance and insertion loss after a few tens of thousands of cycles. For applications where hot switching is needed, improving the reliability of RF-MEMS switches has been a significant challenge. </p>

<img src = "/research/rfmems/hot-rfmems.jpg" style = "display:block; margin-left=auto; margin-right:auto">
<br>

<p> Our group has recently demonstrated an RF-MEMS switch design that can significantly extend the hot-switching life-time of RF-MEMS contact switches. The design concept is shown in the figure above. To prevent the contact degradation during in hot-switching events, a pair of series protection contacts are added in parallel with the "real" contacts. When the switch closes, the protection contacts close first and creates a low-voltage, near cold-switching condition for the "real" contacts. Although protection switches have been proposed in the past, this work combines the protection and "real" contact actuation into a single mechanical structure, and demonstrated unequivocally the significant improvement in hot-switching life-time. For unpackaged devices using Au-Au as the "real" contact material and Pt-Au as the protection contact material, we have demonstrated 150-million actuation cycles at 1-W hot-switching power and 50-million at 2 W. This is much better than anything we have seen!</p>

<p> This design concept can in fact be extended to a few more switch design variations which we are currently investigating. We have also been working on improving the contact materials and packaging for further switch life-time enhancement. </p>

{% assign papers = (site.publication | sort: 'sort_key') %}
<ol reversed>
	{% for paper in papers reversed %}
	{% if paper.topic =="hot-rfmems" %}
	<li>
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
    {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf"  target = "_blank"> <img src = "/images/oa-icon.png"> </a>  </li>
	{% endif %}
	{% endfor %}
</ol>
