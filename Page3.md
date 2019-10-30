<h1>Page 3</h1>

<h1>Random Idiom Using JSON</h1>

<button type="button" class="new-quote button">Show Idiom</button>
 <dl id="quote"></dl>
 
<script>
 //const endpoint = 'https://api.whatdoestrumpthink.com/api/v1/quotes/random';
 //const endpoint = 'https://api.quotable.io/random';
const endpoint = 'https://martinbarge.github.io/sml5202-19-sts/datasets/idioms.json';

function getQuote() {
fetch(endpoint)
.then(function (response) {
return response.json();
})
.then(function(data){
let id = Math.floor(Math.random() * 5);
let idiom = (data.idioms[id].idiom);
let meaning = (data.idioms[id].meaning);
let example = (data.idioms[id].example);

document.querySelector("#quote").innerHTML = "<dt>" + idiom + "</dt>" + "<dd><strong>Example:</strong> " + example + "</dd><dd><strong>Meaning:</strong> " + meaning + "</dd>" ;

//console.log(data.idioms[id].idiom)
})
.catch(function () {
console.log("Error occurred");
});
}

const newQuoteButton = document.querySelector('.new-quote');
newQuoteButton.addEventListener('click', getQuote);

</script>
  

<p>
  <a href="index.html">Home</a> <br>
  <a href="Page2.html">Page2</a>
</p>
