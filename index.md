<h1>Welcome!</h1>

<p> This website is about English language, culture and literature. </p>
<h2> ode to Autum</h2>
<p> 
Season of mists and mellow fruitfulness <br>
close-bosomed friend of the maturing sun<br>
  </p>
  <hr> 
 <p> how to make a cup of Tea </p>
 <ol>
  <li> Boil the water </li>
  <li> pour the water in the mug </li>
  <li> stir and add milk </li>
  </ol>
  <p> How to return an item </p>
<ul>
  <li> go to the post office  </li>
  <li>  drop off your item to the post office </li>
  <li> wait for a refund  </li>
  </ul> 

<h1> Section 1 </h1>

<p>  Hello. My name is Rifa and I am currently studying German with Business
management at Queen Mary University of London. I was born and raised in Germany, lived there my whole childhood 
and then I came to London around 8 years ago. 

Visit my QMULplus Hub page:
<a https://hub.qmplus.qmul.ac.uk/ </a>
</p>

<h1> Section 2 </h1>
<p> Three things I have to do: </p>
<ul> 
<li> Repair my Laptop </li>
<li> Do my Homework </li>
<li> Buy a new charger </li>

<h1> Section 3 </h1> 
<p> Three of my favourite things: </p>
<ol> 
<li> Eating Ice Cream </li>
<li> Reading books </li>
<li> Watching movies </li> 
</ol>

<Hr>
  
  <p>
  <a href="page2.html">Page 2</a> <br>
  <a href="page3.html">Page 3</a>
  </p>

<hr>

<h1>Random Idiom Using JSON</h1>

<button type="button" class="new-quote button">Show Idiom</Button>
<dl id="quote"></dl>



<script>
const endpoint = 'https://rifa23.github.io/SML502-RifaM/datasets/idioms.json';

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

document.querySelector("#quote").innerHTML = "<dt>" + idiom + "</dt>" 
+ "<dd><strong>Example:</strong> "+ example + "</dd><dd><strong>Meaning:</strong> " + meaning + "</dd>" ;

//console.log(data.idioms[id].idiom)
})

.catch(function () {
console.log("Error occurred");
});
}

const newQuoteButton = document.querySelector('.new-quote');
newQuoteButton.addEventListener('click',getQuote);

</script>
