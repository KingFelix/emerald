---
layout: page
title: Search 
---
<!-- Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" placeholder="Search posts...">
<br>
<ul id="results-container"></ul>
</div>

<!-- Script pointing to search-script.js -->
<script src="js/search-script.js" type="text/javascript"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  searchResultTemplate: '<a href="{url}"><li><h3>{title}</h3></li></a>',
  json: '/blog/search.json'
})
</script>
