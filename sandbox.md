---
layout: default
title: Davis Advanced RF Technology
published: true
---
<!--

<div class="container">
  <br>
  <div id="myCarousel" class="carousel slide" data-ride="carousel">

    <ol class="carousel-indicators">
      <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
      <li data-target="#myCarousel" data-slide-to="1"></li>
      <li data-target="#myCarousel" data-slide-to="2"></li>
      <li data-target="#myCarousel" data-slide-to="3"></li>
    </ol>


    <div class="carousel-inner" role="listbox">

      <div class="item active">
        <img src="img_chania.jpg" alt="Chania" width="460" height="345">
        <div class="carousel-caption">
          <h3>Chania</h3>
          <p>The atmosphere in Chania has a touch of Florence and Venice.</p>
        </div>
      </div>

      <div class="item">
        <img src="img_chania2.jpg" alt="Chania" width="460" height="345">
        <div class="carousel-caption">
          <h3>Chania</h3>
          <p>The atmosphere in Chania has a touch of Florence and Venice.</p>
        </div>
      </div>
    
      <div class="item">
        <img src="img_flower.jpg" alt="Flower" width="460" height="345">
        <div class="carousel-caption">
          <h3>Flowers</h3>
          <p>Beatiful flowers in Kolymbari, Crete.</p>
        </div>
      </div>

      <div class="item">
        <img src="img_flower2.jpg" alt="Flower" width="460" height="345">
        <div class="carousel-caption">
          <h3>Flowers</h3>
          <p>Beatiful flowers in Kolymbari, Crete.</p>
        </div>
      </div>
  
    </div>


    <a class="left carousel-control" href="#myCarousel" role="button" data-slide="prev">
      <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="right carousel-control" href="#myCarousel" role="button" data-slide="next">
      <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</div>

-->

### Welcome to the website of the Davis Advanced RF Technologies (DART) lab
<img src="/images/gallery.gif" width="300px" style="float:right; margin-top:10px; margin-left:15px;">

We are a group of researchers with a keen interest in many exciting areas of high frequency electronics. Our research interests include:

- Reconfigurable high frequency devices and components;
- High frequency integrated circuits;
- Millimeter-wave synthetic imaging systems;
- High frequency communication and radar systems and their application in biomedical, societal, and environmental applications.

Critical to our scientific research efforts is a pursuit of fundamental understanding of the physics and engineering principles of high frequency electronics. A major mission of our work is to formulate and disseminate such understanding through university education as well as community outreach.
<!---
The DART lab is housed in Kemper Hall on the beautiful UC Davis campus. The lab is affiliated with the Davis Millimeter-wave Research Center (DMRC). The DMRC is broadly focused on fostering millimeter wave technology for wireless communications, radar, sensing, and imaging systems.
-->

<div class="alert alert-danger">
    A postdoc researcher position is available <strong>immediately</strong>. More details can be found <a href="/people/postdoc-spar.html"> here </a>.
</div>

<div class="alert alert-info">
    A Ph.D. position is available for Fall 2017. Strong analytical capabilities and a background in analog and/or radio frequency IC are preferred.
</div>
<!---
#### A postdoc researcher position is available for 2016. More details can be found [here](/postdoccm.html). 

We are always looking for motivated students and researchers to join the group. Read [more](/joiningdart.html) if you are interested.
-->


{% assign papers = (site.publication | sort: 'sort_key') %}
<ol reversed>
  {% for paper in papers reversed %}
  <li> {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> </li>
  {% endfor %}
</ol>