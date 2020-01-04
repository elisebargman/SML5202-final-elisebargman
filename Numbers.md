<h1>Saying numbers in Spanish</h1>

<p>Just like in English, the pattern for saying numbers out loud in Spanish isn't entirely logical, but it is predictable. Here's how to learn the pattern:</p>

<ol>
 <li>Study up on the pattern using any/all of the following sources:
  <ul>
   <li>hhhh</li>
   <li>bbbb</li>
  </ul>
 </li>
 <li>jjjjj</li>
</ol>

<button type="button" class="new-quote button">New Number</button>
 <dl id="quote"></dl>
 
<script>
const endpoint = 'https://elisebargman.github.io/SML5202-ebargman/datasets/idioms.json';

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

<hr>
