---
title: Pacific Ocean Scenes
layout: rest
description: 
type: parent
order: 3
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "ocean" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
	</div>
</div>