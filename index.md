---
layout: default
title: Davis Advanced RF Technology
published: true
---


### Welcome to the Davis Advanced RF Technologies (DART) lab
<!---
<img src="/images/gallery.gif" width="300px" style="float:right; margin-top:10px; margin-left:15px;">
-->

![Drone](images/daniel_s.jpg "Logo Title Text 1") ![Drone](images/mems1_s.jpg "Logo Title Text 1") ![Drone](images/drone_s.jpg "Logo Title Text 1") ![Drone](images/mems2_s.jpg "Logo Title Text 1") ![Drone](images/liu_s.jpg "Logo Title Text 1") ![Drone](images/osc_s.jpg "Logo Title Text 1")

We are a group of researchers with a keen interest in many exciting areas of high frequency electronics. Our [research](/research/) interests include:

- Reconfigurable high frequency devices and components;
- High frequency integrated circuits;
- High frequency communication and radar systems and their application in biomedical, societal, and environmental applications.

Critical to our scientific research efforts is a pursuit of fundamental understanding of the engineering principles of high frequency electronics. A major mission of our work is to formulate and disseminate such understanding through university [education](/education/) as well as community outreach.
<!---
The DART lab is housed in Kemper Hall on the beautiful UC Davis campus. The lab is affiliated with the Davis Millimeter-wave Research Center (DMRC). The DMRC is broadly focused on fostering millimeter wave technology for wireless communications, radar, sensing, and imaging systems.
-->

<!--
<div class="alert alert-danger">
    A postdoc researcher position is available. More details can be found <a href="/people/postdoc-cm.html"> here </a>.
</div>
-->
<!---
<div class="alert alert-info">
    A Ph.D. position is available for Fall 2017. Strong analytical capabilities and a background in analog and/or radio frequency IC are preferred.
</div>
<!---
#### A postdoc researcher position is available for 2016. More details can be found [here](/postdoccm.html).

We are always looking for motivated students and researchers to join the group. Read [more](/joiningdart.html) if you are interested.
-->


{% for blog in site.blog offset:0 limit:6 %}
  {% if blog.categories contains 'blog' %}
      » [{{ blog.date | date_to_string }}] » <a href="{{ blog.url }}" title="{{ blog.title }}">{{ blog.title }}</a><br>
    {% endif %}
{% endfor %}
