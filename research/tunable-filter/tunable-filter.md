<p> Tunable filters can significantly reduce the complexity of future software-defined frequency- and bandwidth-agile wireless systems. Achieving wide frequency tuning range and a high unloaded quality factor (Qu) at the same time has long been a challenge for tunable filter design and implementations. Highly loaded evanescent-mode cavity filters offer a great balance between the two requirements. </p>

<img src = "/research/tunable-filter/tunable-filter.jpg" style = "display:block; margin-left=auto; margin-right:auto;">
<br>

<p> As a graduate student, Dr. Liu pioneered the use of electrostatic micro-electromechanical actuators for the implementation of high-Q tunable evenescent-mode filters. An electronic tunable 2-pole filter was demonstrated for 3-4.7 GHz with 0.7% fractional bandwidth, insertion loss of 3.6-2.4 dB, and extracted Qu of 300-600. Further works demonstrated tunable bandpass and bandstop filters with similarly high Qu and tuning range for frequencies up to 20 GHz. </p>

<p> At UC Davis, we have continued the work exploring various aspects of the design and fabrication of novel tunable filters. We have demonstrated a design strategy for integrating lumped tuning elements with cavity filters. We have also introduced a frequency and bandwidth tunable filter design method based on dispersive coupling structures, showing bandwidth tunability of 0-10%. At the 0% bandwidth state, this coupling structure effectively shuts off the filter and can work as an RF switch without relying on an actual switch. More recently, we have also demonstrated a W-band (75-110 GHz) waveguide tunable filter with recording-breaking tunability and insertion loss. </p>

<ol reversed>
	{% for paper in papers reversed %}
	{% if paper.topic =="tunable-filter" %}
	<li>
    {% if paper.note != null %}
		<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
	{% endif %}
    {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf"  target = "_blank"> <img src = "/images/oa-icon.png"> </a> </li>
	{% endif %}
	{% endfor %}
</ol>
