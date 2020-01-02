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


<hr>
  <html lang="fr">
  <table>
    <tr><th>Colour</th><th>Translation(1<sup>er</sup>personne sing.)</th></tr>
    <tr><td>Blue</td><td>Bleu(e)</td>
    <tr><td>Green</td><td>Vert(e)</td>
    <tr><td>Red</td><td>Rouge</td>
    <tr><td>Pink</td><td>Rose</td>
    <tr><td>Grey</td><td>Gris(e)</td>
    <tr><td>Black</tf><td>Noir(e)</td>
