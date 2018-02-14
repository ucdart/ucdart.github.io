---
layout: default
title: Davis Advanced RF Technology
published: true
---
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
		jQuery(document).ready(function($) {
			$('.fading-slider').unslider({
				animation: 'fade',
				autoplay: true,
			arrows: false
			});
		});
	</script>
</div>

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