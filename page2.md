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
