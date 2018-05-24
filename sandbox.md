---
layout: default
title: Davis Advanced RF Technology
published: true
---
{% assign papers = (site.publication | sort: 'sort_key') %}
<ol reversed>
	{% for paper in papers offset:0 limit:3 %}
		{% if paper.type =="article" %}
		<li>     
    		{% if paper.note != null %}
				<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
			{% endif %}
    		{{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> <i> {{ paper.journal }}</i>, vol. {{ paper.volume }}, no. {{ paper.number }}, pp. {{ paper.pages }}, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf" target = "_blank"> <img src = "/images/oa-icon.png"> </a>
		</li>
	{% elseif paper.type =="conference" %}
		<li>
			{% if paper.note != null %}
			<span style='font-weight:600; color:#AD655F;'>[{{ paper.note }}]</span> &nbsp;
		{% endif %}
			 {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }},"</span> <i> {{ paper.booktitle}}</i>, {{ paper.month }}, {{ paper.year }}. &nbsp; <a href="http://dx.doi.org/{{ paper.doi }}">DOI:{{ paper.doi }}</a> | <a href = "/publication/{{ paper.bib_key}}.pdf"  target = "_blank"> <img src = "/images/oa-icon.png"> </a> </li>
	{% endif %}
	{% endfor %}
</ol>

{% assign papers = (site.publication | sort: 'sort_key') %}
{{ papers[-3:0].author }}

<!--

<h2>Automatic Slideshow</h2>
<p>Change image every 2 seconds:</p>

<div class="slideshow-container">

<div class="mySlides fade">
  <div class="numbertext">1 / 3</div>
  <img src="images/img_nature_wide.jpg" style="width:100%">
  <div class="text">Caption Text</div>
</div>

<div class="mySlides fade">
  <div class="numbertext">2 / 3</div>
  <img src="images/img_fjords_wide.jpg" style="width:100%">
  <div class="text">Caption Two</div>
</div>

<div class="mySlides fade">
  <div class="numbertext">3 / 3</div>
  <img src="images/img_mountains_wide.jpg" style="width:100%">
  <div class="text">Caption Three</div>
</div>

</div>
<br>

<div style="text-align:center">
  <span class="dot"></span>
  <span class="dot"></span>
  <span class="dot"></span>
</div>

<script>
var slideIndex = 0;
showSlides();

function showSlides() {
    var i;
    var slides = document.getElementsByClassName("mySlides");
    var dots = document.getElementsByClassName("dot");
    for (i = 0; i < slides.length; i++) {
       slides[i].style.display = "none";  
    }
    slideIndex++;
    if (slideIndex > slides.length) {slideIndex = 1}    
    for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
    }
    slides[slideIndex-1].style.display = "block";  
    dots[slideIndex-1].className += " active";
    setTimeout(showSlides, 4000); // Change image every 2 seconds
}
</script>

-->
<div class="container">
  <h2>Carousel Example</h2>  
  <div id="myCarousel" class="carousel slide" data-ride="carousel">
    <!-- Indicators -->
    <ol class="carousel-indicators">
      <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
      <li data-target="#myCarousel" data-slide-to="1"></li>
      <li data-target="#myCarousel" data-slide-to="2"></li>
    </ol>

    <div class="carousel-inner">
      <div class="item active">
        <img src="images/img_nature_wide.jpg" alt="Los Angeles" style="width:100%;">
      </div>

      <div class="item">
        <img src="images/img_fjords_wide.jpg" alt="Chicago" style="width:100%;">
      </div>

      <div class="item">
        <img src="images/img_mountains_wide.jpg" alt="New york" style="width:100%;">
      </div>
    </div>


    <a class="left carousel-control" href="#myCarousel" data-slide="prev">
      <span class="glyphicon glyphicon-chevron-left"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="right carousel-control" href="#myCarousel" data-slide="next">
      <span class="glyphicon glyphicon-chevron-right"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</div>

<hr>

<div>
<h2> fading slider demo </h2>
	<div class="fading-slider">
		<ul>
			<li><img src="images/img_nature_wide.jpg" alt="Cats!"></li>
			<li><img src="images/img_fjords_wide.jpg" alt="Cats!"></li>
			<li><img src="images/img_mountains_wide.jpg" alt="Cats!"></li>
		</ul>
	</div>
	<script>
		$('.fading-slider').unslider({
			autoplay: true,
			arrows: false
		});
	</script>
</div>


#Full Publication List
{% assign papers = (site.publication | sort: 'sort_key') %}
<ol reversed>
  {% for paper in papers reversed %}
  <li> {{ paper.author }}, <span style='font-weight: 600;'>"{{ paper.title }}," </span> </li>
  {% endfor %}
</ol>
