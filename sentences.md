<hr>
<h1>Articles</h1>
<p>Ici, nous allons apprendre les articles féminins, masculins et pluriels en français. <i>Here, we are going to learn the feminine, masculine and plural articles in French</i></p>

  <html lang="fr">
  <table>
    <tr><th>Article</th><th>Translation</th></tr>
    <tr><td>I</td><td>Je(e)</td>
    <tr><td>You (informal, singular)</td><td>Tu(e)</td>
    <tr><td>He</td><td>Il</td>
    <tr><td>She</td><td>Elle</td>
    <tr><td>We/It</td><td>On(e)</td>
    <tr><td>Us</td><td>Nous(e)</td>
    <tr><td>You (formal, singular)</td><td>Vous(he)</td>
    <tr><td>Ils (a group of masculine subjects or a mixed group)</td><td>Ils(te)</td>
    <tr><td>Elles (a group of feminine subjects)</td><td>Elles</td>
     
<iframe src="https://h5p.org/h5p/embed/689078" width="1090" height="526" frameborder="0" allowfullscreen="allowfullscreen"></iframe><script src="https://h5p.org/sites/all/modules/h5p/library/js/h5p-resizer.js" charset="UTF-8"></script>

<h2>Adjectifs<a href="https://intisarmusa.github.io/sml5202-intisar/vocabulary.html">refer to adjectives here</a></h2>

<iframe src="https://h5p.org/h5p/embed/689087" width="1090" height="307" frameborder="0" allowfullscreen="allowfullscreen"></iframe><script src="https://h5p.org/sites/all/modules/h5p/library/js/h5p-resizer.js" charset="UTF-8"></script>

<h2>Verbes<a href="https://intisarmusa.github.io/sml5202-intisar/vocabulary.html">refer to verbs here</a></h2>

<iframe src="https://h5p.org/h5p/embed/689091" width="1090" height="276" frameborder="0" allowfullscreen="allowfullscreen"></iframe><script src="https://h5p.org/sites/all/modules/h5p/library/js/h5p-resizer.js" charset="UTF-8"></script>









































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
 
 
 <h1>Create Sentences</h1>
<button onclick="makeSentence()">Make Sentence</button>


<p id="demo"></p>


<h1>Create Sentences</h1>
<button onclick="makeSentence()">Make Sentence</button>


<p id="demo"></p>


<script>
function makeSentence(){
var person = {
    names: [ "Jacob", "Mark", "Brian", "Lucas", "Johnny", "Joshua", "He", "She", "Jae" ],
    verbs: [ "speaks", "eats", "drinks", "walks", "sleeps", "studies", "sings", "runs", "dances" ],
    adverbs: [ "slowly", "quickly", "noisily", "badly", "cheerfully"]
};

var i;
var text = "";
for(i = 0; i < person.names.length; i++) {
name = person.names[i];
verb = person.verbs[Math.floor(Math.random() * person.verbs.length)];
adverb = person.adverbs[Math.floor(Math.random() * person.adverbs.length)];

text += name + " " + verb + " " + adverb + ".<br>"

document.getElementById("demo").innerHTML = text;

}
}

</script>

