<h1>Saying numbers in Spanish</h1>

<p>Just like in English, the pattern for saying numbers out loud in Spanish isn't entirely logical, but it is predictable. Here's how to learn the pattern:</p>

<ol>
 <li>Study up on numbers in Spanish using any/all of the following language learning sources:
  <ul>
   <li><a href="https://www.fluentin3months.com/spanish-numbers/">Fluent in 3 Months</a></li>
   <li><a href="https://www.mezzoguild.com/spanish-numbers/">The Mezzofanti Guild</a></li>
   <li><a href="https://spanishnumbers.guide/numbers-in-spanish.html">Spanish Numbers Guide</a></li>
   <li><a href="https://www.youtube.com/watch?v=iVyUMBmfDiY">Butterfly Spanish (video)</a></li>
   <li>My video below</li>
  </ul>
 </li>
 <li>Practice your audio comprehension of numbers with the Number Writing activity</li>
 <li>Practice your spoken pronunciation of numbers with the Saying Numbers activity</li>
</ol>
<br>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Psvj8s4_yHk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<h2>Number Writing</h2>
<iframe src="https://h5p.org/h5p/embed/689524" width="1090" height="842" frameborder="0" allowfullscreen="allowfullscreen"></iframe><script src="https://h5p.org/sites/all/modules/h5p/library/js/h5p-resizer.js" charset="UTF-8"></script>

<h2>Saying Numbers</h2>
<p> Click the buttons for the ranges of numbers that you need to practice with, and then try saying them out loud</p>

<button onclick="document.getElementById('demo4').innerHTML = getRndInteger(1800,2100)">Years</button>
<p id="demo4"></p>

<button onclick="document.getElementById('demo').innerHTML = getRndInteger(0,20)">0 to 20</button>
<p id="demo"></p>

<button onclick="document.getElementById('demo1').innerHTML = getRndInteger(20,100)">20 to 100</button>
<p id="demo1"></p>

<button onclick="document.getElementById('demo2').innerHTML = getRndInteger(100,1000)">100 to 1,000</button>
<p id="demo2"></p>

<button onclick="document.getElementById('demo3').innerHTML = getRndInteger(1000,1000000000)">1,000 to 1,000,000,000</button>
<p id="demo3"></p>

<button onclick="document.getElementById('demo5').innerHTML = getRndInteger(1000000000,100000000000000)">Extreme Challenge Mode: "Billions" and "Trillions"?</button>
<p id="demo5"></p>

<script>
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min)) + min;
}</script>
