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
<!-- ![image-title-here](/img/Trump.jpg){:class="img-responsive"} -->

The Panama papers were released in 2015, they constitue the biggest leak of financial information in history before the recent Paradise papers leak. It first came from the Panamanian corporate service company Mossack Fonseca. The leak revealed a substantial amount of illegal activities including fraud and tax evasion. It especially revealed illegal financial activities carried out by world's biggest wealth holders, politicians and companies. A leak of that size is a very powerful tool to attest the poor behaviour of hundreds of thousands entities. Obviously the Panama Papers are not an exhaustve list of the hidden financial activities. 



#### Panama papers in numbers
 
-The Panama Papers are 11.5 million leaked documents that detail financial and attorney–client information for more than 214,488 offshore entities. Some 4.8 million leaked files were emails, 3 million were database entries, 2.2 million PDFs, 1.2 million images, 320,000 text files, and 2242 files in other formats. Journalists from 107 media organizations in 80 countries analyzed documents detailing the operations of the law firm. After more than a year of analysis, the first news stories were published on April 3, 2016, along with 150 of the documents themselves.
-The sheer quantity of leaked data greatly exceeds the WikiLeaks Cablegate leak in 2010 (1.7 GB), Offshore Leaks in 2013 (260 GB), the 2014 Lux Leaks (4 GB), and the Swiss Leaks (3.3 GB) of 2015. For comparison, the Panama Papers equals approximately 2,660 GB.



#### A word about Paradise papers before starting
This website is dedicated to the presentation of a data analysis project concerning the Paradise Papers. The project mainly consists in developing tools to better understand the geographical structure of the off-shore leak The data employed for this project are taken from the International Consortium of Investigative Journalist (ICIJ) website. You might not have missed the fact that recently a leak of comparable importance with the Panama papers leak has been released: the Paradise papers. The latter has also been released by the ICIJ and beneficiate from the same data formatting as the Panama papers. Therefore luckily we are at one step to extend the implementation of the tools that we are going to show you with the Paradise papers. 






### Panama papers in numbers

--- 

### Outline of the project

This project aims to compile the information provided by the Panama papers to show the geographical structure of offshore activities. We intend to do so thanks to an interactive map showing connections between the different entities and officers concerned by the leak. The idea being to make the information shown on the map scalable.   
  
**Reserch questions :**   
- Which countries were the most involved in the offshore activities unveiled in the leak?   <br>
- What are the relationships between countries and tax heavens?  <br>
- Where does corruption come from ?  <br>  
	
We strongly believe in the usefulness of this kind of project in order to get a better understanding of the worldwide organization of the tax evasion phenomenon. We think that it could help society realize the importance of the event. It could therefore push towards the implementation of new tax regulations to prevent such aberrance. 








----
  
### Tax Evasion

From our analysis it becomes very clear they are few countries able to attract, keep and hide large amount of money from foreign tax authorities. It is clear the main incentive to create offshore accounts/companies is the savings on taxes allowed by a lack of economic policies in those countries.     
The pattern to tax evasion becomes almost simple when spotlighted. A company or private individual may create a "Shell company" in the country of his choice, preferably where regulations are weak, for example, no need to name the owner. These shell companies, also called Offshore Entites, are usually limited liability companies and don't conduct any business, they just own financial assets of their owner. To fullfill a tax evasion, they also need a go-between with a service provider, these intermadiaries usually are law-firms, banks or middlemen that asks an offshore service provider to create an offshore firm for a client. Finally, bearers are the entites receiving shares from an offshore company, unfortunatly bearer shares provide one of the deepest levels of secrecy. 
{% include Trump.html %}  <br>



  
Nomenclature:  
- **Offshore Entity** : A company, trust or fund created in a low-tax, offshore jurisdiction by an agent.   
- **Officer** : A person or company who plays a role in an offshore entity.   
- **Intermediary**: A go-between for someone seeking an offshore corporation and an offshore service provider -- usually a law-firm or a middleman that asks an offshore service provider to create an offshore firm for a client.  
 
 
<br>   
<br>   

---

### Leading Actors
The map above shows the worldwode distribution of the three main kinds of actors : which are Offshore entites, Intermediaries and Officers. We notice those three differs from each other on a global scale even though some countries are well represented in all three cathegories. 
Regarding the offshore entities, we must notice the precence of the three economic global powers : USA, China and Russia. But they are, by far, not the more effcicient hosting countries. Indeed, in Europe, Switzerland is leading with more than 37 thousands hosted entites (10 times more than Russia), followed by Luxembourg and Great Britain. In South America, Panama has a large carpital of offshore entites. In western Asia, EAU is also leading.
The Intermediaries are once again most located in Switzerland and Grat Britain, as they are known for the privacy of their bank services. Still, the distribution of the intermediaries is very similar to the offsore entites distribution on a blobal scale.
Finally, we notice the southern countries are more involved in the officer distribution. Usualy officiers are settled in different jurisdiction than the company/private individual at the origin of the tax evasion.

  
{% include multi_carte.html %}	 <br>

### Queries

From the raw dataset, we were able to designe a tool to query for types, names and locations 
The provided dataset allow us to investigate for specific relationships  



---

### Web App

--

### Full Project

The full project is available on a [github repository](https://github.com/adrienruault/ada_molmaru/tree/master/project). It provides a Jupyter Notebook processing the data from the Panama Papers & Paradise Paper with a performant query tool to geographically display portions of actors involved in cash criminality. This tool was not implemented in this html page due to a lack of time and compliance between python's libraries and html.   
The datasets was downloaded from [The International Consortium of Investigative Journalists](https://offshoreleaks.icij.org/pages/database) website.


### Gallery


{% include Cahuzac.html %}

{% include Sigmundur.html %}

{% include ANG_VONG_VATHANA.html %}

{% include FIFA1.html %}


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
