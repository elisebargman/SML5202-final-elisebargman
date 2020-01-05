<h1>More Resources</h1>


<p>This page is designed to send you on your way with all the resources you'll need to continue your Spanish language journey, including dictionaries and translation tools, top-rated language learning apps, and media recommendations to immerse yourself in other cultures.</p>

<section>
	<h3>Tools & Resources</h3>
<ul>
  <li><a href="https://translate.google.com/">Google Translate</a></li>
  <li><a href="https://studyspanish.com/typing-spanish-accents">Typing the Spanish alphabet</a></li>
  <li><a href="https://www.asihablamos.com/">AsiHablamos</a> (a dictionary of slang terms, similar to Urban Dictionary)</li>
  <li><a href="https://www.rae.es/recursos/diccionarios">Dictionaries of the Royal Spanish Academy</a> (take everything they say with a <a href="https://www.nytimes.com/2010/11/26/world/europe/26spanish.html">grain of salt</a>)</li>
</ul>
</section>

<section>
	<h3>Seven fun ways to continue practicing your Spanish:</h3>
<ol>
	<li>Find a <a href="https://www.fluentin3months.com/pen-pals/">language-learning pen pal</a></li>
	<li>Stay up-to-date with Latin Americannewspapers, like <a href="https://www.univision.com">Univision</a> and <a href="https://www.eltiempo.com/">El Tiempo</a></strong></li>
	<li>Use a <a href="https://www.cnet.com/news/best-language-learning-apps-become%20fluent/">well-reviewed</a> mobile language learning app, such as <a href="https://www.duolingo.com/">Duolinguo</a>, <a href="https://www.babbel.com/">Babbel</a>, or <a href="https://www.memrise.com/">Memrise</a></li>
	<li>Listen to the <a href="https://www.newsinslowspanish.com/spanish-podcast">News in Slow Spanish</a> podcast on <a href="https://open.spotify.com/show/3DfaUnQ6qypI0qK7tGhp4A">Spotify</a></li>
	<li>Read the Spanish versions of your favorite magazines, like <a href="https://www.ngenespanol.com/">National Geographic</a> and <a href="https://www.seventeenenespanol.com/">Seventeen</a></li>
	<li>Watch some great Spanish television, <a href="https://spanishlandschool.com/best-spanish-tv-shows/">written with language learners in mind</a></li>
	<li>Go down a "Wikipedia en Español" rabbit hole... see below to get started!</li>
</ol>
</section>

<header class="searchForm-container">
<img src="https://image.ibb.co/e6vOFQ/wikipedia.png" alt="Wikipedia Logo">
<form class="searchForm">
        <input type="search" class="searchForm-input">
        <button type="submit" class="icon searchIcon">
          <img src="https://image.ibb.co/cpG8zk/search.png" alt="Magnifying Glass Icon">
        </button>
        <a href="" class="icon randomIcon">
          <img src="https://image.ibb.co/fR5OX5/random.png" alt="Shuffle Icon">
        </a>
      </form>
</header>
<section class="searchResults"></section>
  
<script>
  function handleSubmit(event) {
    // prevent page from reloading when form is submitted
  event.preventDefault();
  // get the value of the input field
  const input = document.querySelector('.searchForm-input').value;
  // remove whitespace from the input
  const searchQuery = input.trim();
  // call `fetchResults` and pass it the `searchQuery`
  fetchResults(searchQuery);
}

function fetchResults(searchQuery) {
	  const endpoint = `https://es.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=${searchQuery}`;
  	fetch(endpoint)
  		.then(response => response.json())
  		.then(data => {
        const results = data.query.search;
  	  	displayResults(results);
		})
       .catch(() => document.querySelector('.searchForm-input').value = 'Please enter a search term.');
       //.catch(() => console.log('An error occured'));
}

function displayResults(results) {
  const searchResults = document.querySelector('.searchResults');
  searchResults.innerHTML = '';
  results.forEach(result => {
  const url = encodeURI(`https://es.wikipedia.org/wiki/${result.title}`);
  
  searchResults.insertAdjacentHTML('beforeend',
  
  `<div class="resultItem">
  <h3 class="resultItem-title">
  <a href="${url}" target="_blank" rel="noopener">${result.title}</a>
  </h3>
  <span class="resultItem-snippet">${result.snippet}</span><br>
  <a href="${url}" class="resultItem-link" target="_blank" rel="noopener">${url}</a>
  </div>`
  );
  
});

console.log(results);
}
const form = document.querySelector('.searchForm');
form.addEventListener('submit', handleSubmit);
</script>

<hr>
<div style="clear:both;"></div>
<div>
	<p style="font-size: 86%;">Credit: The code for this application is derived from an excellent online tutorial by Ayooluwa Isaiah, a Web Technologies Software Developer based in Lagos, Nigeria. The tutorial can be followed <a href="https://freshman.tech/wikipedia-javascript/">here</a>.</p></div>

