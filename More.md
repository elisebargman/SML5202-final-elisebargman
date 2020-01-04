<h1>More Resources</h1>


<p>This page is designed to send you on your way with all the resources you'll need to continue your language learning journey, including translation tools, top-rated language learning apps, and media recommendations to immerse yourself in the language and culture.</p>

<ul>
  Resources:
  <li><a href="https://translate.google.com/">Google Translate</a></li>
  <li><a href="https://studyspanish.com/typing-spanish-accents">Typing the Spanish alphabet</a></li>
</ul>

<ul>
  Best language learning applications, according to <a href="https://www.cnet.com/news/best-language-learning-apps-become fluent/">CNET</a>: 
  <li><a href="https://www.duolingo.com/">Duolinguo</a></li>
  <li><a href="https://www.babbel.com/">Babbel</a></li>
  <li><a href="https://www.memrise.com/">Memrise</a></li>
</ul>

<ol>
  Top ten ways to continue practicing your Spanish:
  <li><a href="https://translate.google.com/">Google Translate</a></li>
  <li><a href="https://studyspanish.com/typing-spanish-accents">Typing the Spanish alphabet</a></li>
</ol>
  

  
Explore:
https://es.wikipedia.org/wiki/Idioma_espa%C3%B1ol
Wikipedia: Idioma Español

https://www.newsinslowspanish.com/spanish-podcast
News in Slow Spanish
https://open.spotify.com/show/3DfaUnQ6qypI0qK7tGhp4A
Find it on Spotify

https://www.univision.com
Univision
https://digital.revisbarcelona.com/
Revista Barcelona (Argentinian satire)
https://www.eltiempo.com/
El Tiempo (Colombia)

https://www.ngenespanol.com/
National Geographic en español
https://www.seventeenenespanol.com/
Seventeen en español
https://www.gq.com.mx/
GQ en español


https://spanishlandschool.com/best-spanish-tv-shows/


Resources:
Google Translate
Typing the Spanish alphabet

Best language learning applications, according to CNET:
Duolingo
Babbel
Memrise

Explore:
Wikipedia: Idioma Español
News in Slow Spanish
Find it on Spotify
Univision
Revista Barcelona (Argentinian satire)
El Tiempo (Colombia)
National Geographic en español
Seventeen en español
GQ en español


</p>

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
	  const endpoint = `https://en.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=${searchQuery}`;
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
  const url = encodeURI(`https://en.wikipedia.org/wiki/${result.title}`);
  
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


