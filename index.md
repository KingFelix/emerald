---
layout: page
title: Panama Papers
subtitle: Where does the money come from ?
use-site-title: true
---

# Dataset

The dataset is available too everyone and free to use.

# Processing of the Data
The data has some miising value we had to discard.

# Handle of the Data
The data is small enough to process it on our personnal laptops.

# Display information
We used folium library to display the location of the entites 


[//]:#(---------- END OF WHAT IS VISIBLE ----------------)
<!-- Posts -->
<ul id="posts">

	{% for post in paginator.posts %}

	  <li class="post">
	  	<h2><a href="{% if site.baseurl == "/" %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">{{ post.title }}</a></h2>
		<time datetime="{{ post.date | date_to_xmlschema }}" class="by-line">{{ post.date | date_to_string }}</time>
	  	<p>{{ post.content | strip_html | truncatewords:50 }}</p>
	  </li>

   {% endfor %}

</ul>
