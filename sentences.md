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

