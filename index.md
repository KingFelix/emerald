---
layout: default
title: Panama Papers
subtitle: Where does the money come from ?
use-site-title: true
published: true
---
## {{page.subtitle}}  
<br>   
<br>   
  
### Introduction to the Panama Papers

The Panama papers were released in 2015, they constitue the biggest leak of financial information in history. It first came from the Panamanian corporate service company Mossack Fonseca. The leak revealed a substantial amount of illegal activities including fraud and tax evasion. It especially revealed illegal financial activities carried out by world's biggest wealth holders, politicians and companies.  
A leak of that size is a very powerfull tool to attest the poor behaviour of hundreds of thousands entities, although it doesn't guarantee the good behaviour of those who are not listed in the database .

### Outline of the project

This project aims to compile the information provided by the Panama papers to show the geographical structure of offshore activities. We intend to do so thanks to an interactive map showing connections between the different entities and officers concerned by the leak. The idea being to make the information shown on the map scalable.   
  
Reserch questions :   
&nbsp; - Which countries were the most involved in the offshore activities unveiled in the leak?   <br>
&nbsp; - What are the relationships between countries and tax heavens?  <br>
&nbsp; - Where does corruption come from ?  <br>  
	
We believe the a good understanding of the tax evasion could lead to the implementation of new tax regulations to prevent such aberrance.  
<br> 
 


### Tax Evasion

From our analysis it becomes very clear they are few countries able to attract, keep and hide large amount of money from foreign tax authorities. It is clear the main incentive to create offshore accounts/companies is the savings on taxes allowed by a lack of economic policies in those countries.     
The pattern to tax evasion becomes almost simple when spotlighted. A company or private individual may create a "Shell company" in the country of his choice, preferably where regulations are weak, for example, no need to name the owner. These shell companies, also called Offshore Entites, are usually limited liability companies and don't conduct any business, they just own financial assets of their owner. To fullfill a tax evasion, they also need a go-between with a service provider, these intermadiaries usually are law-firms, banks or middlemen that asks an offshore service provider to create an offshore firm for a client. Finally, bearers are the entites receiving shares from an offshore company, unfortunatly bearer shares provide one of the deepest levels of secrecy. 
   
  
  
Nomenclature:  
&nbsp; **- Offshore Entity** : A company, trust or fund created in a low-tax, offshore jurisdiction by an agent.   
&nbsp; **- Officer** : A person or company who plays a role in an offshore entity.   
&nbsp; **- Intermediary**: A go-between for someone seeking an offshore corporation and an offshore service provider -- usually a law-firm or a middleman that asks an offshore service provider to create an offshore firm for a client.  
 
{% include multi_carte.html %}
 
<br>   
<br>   
  
### Leading Actors
The map above shows the worldwode distribution of the three main kinds of actors : which are Offshore entites, Intermediaries and Officers. We notice those three differs from each other on a global scale even though some countries are well represented in all three cathegories. 
Regarding the offshore entities, we must notice the precence of the three economic global powers : USA, China and Russia. But they are, by far, not the more effcicient hosting countries. Indeed, in Europe, Switzerland is leading with more than 37 thousands hosted entites (10 times more than Russia), followed by Luxembourg and Great Bretain. In South America, Panama has a large carpital of offshore entites. In western Asia, EAU is also leading.
The Intermediaries are once again most located in Switzerland and Grat Bretain, as they are known for the privacy of their bank services. Still, the distribution of the intermediaries is very similar to the offsore entites distribution on a blobal scale.
Finally, we notice the southern countries are more involved in the officer distribution. Usualy officiers are settled in different jurisdiction than the company/private individual at the origin of the tax evasion.


### Full Project

The full project is available on a [github repository](https://github.com/adrienruault/ada_molmaru/tree/master/project). It provides a Jupyter Notebook processing the data from the Panama Papers & Paradise Paper with a performant query tool to display geographically portions of actors involved in cash criminality.The datasets was downloaded from [The International Consortium of Investigative Journalists](https://offshoreleaks.icij.org/pages/database) website.











[//]:#(---------- END OF WHAT IS VISIBLE ----------------)<!DOCTYPE html>


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
