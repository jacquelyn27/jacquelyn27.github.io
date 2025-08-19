---
title: home
layout: home
type: parent
order: 1
---

<div class="section header">
	<div class="container">
		<img src="{{ "/assets/img/logo.png" | relative_url }}"><!-- should be svg -->
		<h3 class="section-heading">watercolors</h3>
		<!--
		<p class="section-description">
		</p>
		-->
		<div id="navbar-wrapper">
			<div id="navbar">
				<img id="brand" class="hide" src="{{ "/assets/img/logo.png" | relative_url }}">
				{% assign mypages = site.pages | where: "type", "parent" | sort: "order" %}
				{% for page in mypages %}
				<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
				{% endfor %}
			</div>
		</div>
	</div>
</div>

<<<<<<< Updated upstream
<<<<<<< Updated upstream
<img src="/images/jacquelyn_coleman.png" alt="Jacquelyn Coleman" width="150" float="right" style="margin-left: 20px; margin-bottom: 20px;border-radius: 10%;">

Jacquelyn Coleman is a watercolorist known for her evocative depictions of the California landscape, particularly the Monterey Bay Area. Her work captures the essence of everyday life and the natural beauty of her surroundings, reflecting a deep connection to the places she paints.

![Carmel Mission](images/carmel_mission.png)
*Carmel Mission*

Jacquelyn Coleman's approach to watercolor has its roots in the California Style of watercolor painting, part of the American Scene or Regionalist movement that swept across the United States during the mid twentieth century. She spent many of the early years of her career painting weekly on location with artist George Post, documenting scenes and activities of everyday life in San Francisco and the greater San Francisco Bay Area. She later studied with California watercolorists Rex Brandt, Jade Fon, and Richard Yip.

In the early 1970s, a mother of five children, Jacquelyn maintained an active watercolor practice while also playing a prominent role in the Bay Area arts community. She served as board member of the Oakland Art Association, President of the Art League of the East Bay, and in 1975 was elected president of the San Francisco Women Artists.

The next year she and her family moved to Connecticut where, painting with Charles Reid, her work became focused on figure studies and still lifes. She painted at Studio 3 in Westport, showed at Silvermine Gallery in Connecticut as well as in traveling exhibits with the American Watercolor society. She continued study of life drawing at the National Academy of Art in New York city and went on to win their General Electric prize in a juried show. Her work won the President's prize at the Wadsworth Atheneum Museum at Harford, Connecticut. The figure painting, Lady in Profile, earned her a signature membership in the American Watercolor Society (AWS), placing Jacquelyn among  selected for this honor including Jamie Wyeth, Dong Kingman, E. Raymond Kinstler, and Janet B. Walsh.

Later, when she and her husband owned a summer property in Boothbay Harbor, Maine, she turned again to painting en plein air, this time water scenes, which she continued after moving to Carmel, California. While Jacquelyn has painted in numerous countries around the world, including Italy, France and China, most of her work is influenced by the natural beauty of the Monterey Bay Area and northern California coastline. Her paintings of the Carmel Mission and the Carmel Library have been selected as representative images of those two Carmel landmarks.

![San Francisco Victorian](images/sanfrancisco_victorian.png)


---

*© {{ page.date | date: "%Y" }} Jacquelyn Coleman. All rights reserved.*
=======
=======
>>>>>>> Stashed changes
<div class="section main">
	<div class="container">
		<div class="row" id="gallery">
			{% assign coll = site.collections | where: "label", "home" | first %}
			{% assign list = coll.files | sort: "basename" %}
			<!--{% assign l = coll.files.size | divided_by: 2 | ceil %}-->
			<div class="column">
				{% for image in list limit: 5 %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
			<!--<div class="one-half column">
				{% for image in list offset: l %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>-->
		</div>
	</div>
<<<<<<< Updated upstream
</div>
>>>>>>> Stashed changes
=======
</div>
>>>>>>> Stashed changes
