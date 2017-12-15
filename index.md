---
layout: page
title: Panama Papers
subtitle: Where does the money come from ?
use-site-title: true
---

# Dataset

# Processing of the Data

# Handle of the Data

# Display information

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
