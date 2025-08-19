---
title: home
layout: home
nav: true
order: 1
---

<div class="section header">
	<div class="container">
		<img src="{{ "/assets/img/logo.png" | relative_url }}"><!-- should be svg -->
		<h3 class="section-heading">California Watercolorist</h3>
		<p class="section-description">
Jacquelyn Coleman is a watercolorist known for her<br />evocative depictions of the California landscape. <br />Her work captures the essence of everyday life <br />and the natural beauty of her surroundings, <br />reflecting a deep connection to the places she paints.
		</p>
		<div id="navbar-wrapper">
			<div id="navbar">
				<img id="brand" class="hide" src="{{ "/assets/img/logo.png" | relative_url }}">
				{% assign mypages = site.pages | where: "nav", true | sort: "order" %}
				{% for page in mypages %}
				<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
				{% endfor %}
			</div>
		</div>
	</div>
</div>

<div class="section main">
	<div class="container">
		<div class="row" id="gallery">
			{% assign coll = site.collections | where: "label", "home" | first %}
			{% assign list = coll.files | sort: "basename" %}
			<!--{% assign l = coll.files.size | divided_by: 2 | ceil %}-->
			<div class="column">
				{% for image in list limit: 1 %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
		</div>
	</div>
</div>
