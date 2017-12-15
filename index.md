---
layout: default
title: Panama Papers
subtitle: Where does the money come from ?
use-site-title: true
---
## {{page.subtitle}}  
  
   

### Introduction to the Panama Papers

The Panama papers were released in 2015, they constitue the biggest leak of financial information in history. It first came from the Panamanian corporate service company Mossack Fonseca. The leak revealed a substantial amount of illegal activities including fraud and tax evasion. It especially revealed illegal financial activities carried out by world's biggest wealth holders, politicians and companies.  
A leak of that size is a very powerfull tool to attest the poor behaviour of hundreds of thousands entities, although it doesn't guarantee the good behaviour of those who are not listed in the database .

### Outline of the project

This project aims to compile the information provided by the Panama papers to show the geographical structure of offshore activities. We intend to do so thanks to an interactive map showing connections between the different entities and officers concerned by the leak. The idea being to make the information shown on the map scalable.   

###### Reserch questions :
  
  We believe the a good understanding of the tax evasion could lead to the implementation of new tax regulations to prevent such aberrance.
- Which countries were the most involved in the offshore activities unveiled in the leak?
- What are the relationships between countries and tax heavens?
- Where does corruption come from ?

### Tax Evens

From our analysis it becomes very clear they are very few countries able to attract, keep and hide large amount of money from foreign tax authorities. It is clear the main incentive to create offshore accounts/companies is the savings on taxes allowed by a lack of economic policies in those countries.     
The pattern to tax evasion becomes almost simple when spotlighted. A company or private individual may create a "Shell company" in a country of his choice, preferably where regulations are weak, for example, no need to name the owner. These shell companies, also called Offshore Entites, are usually limited liability companies and don't conduct any business, they just own financial assets of their owner. To fullfill a tax evasion, you also need a go-between with a service provider, These intermadiaries usually are law-firms, banks or a middlemen that asks an offshore service provider to create an offshore firm for a client. Finally, bearers are the entites receiving shares from an offshore company, unfortunatly bearer shares provide one of the deepest levels of secrecy. 
   
   
Add map

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
