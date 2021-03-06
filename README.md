# Javascript, cheat sheet. 

- Les variables [## Les variables]
- Les tableaux
- Conditions : if, else
- [Les événements](#Les-événements) 


## Les bases

```javascript 
var string = "Steve"; //Ceci est une chaine de caractère.
var nombre = 4;       //Ceci est un nombre. 
var boolean = true;   //Ceci est un booléen, qui ne peut être qu'égal à vrai ou faux, donc true ou false. 
var monTableau = ["Un", "Deux", "Trois", "Quatre", "Cinq", "Six"]; // Le tableau permet de stocker plusieurs valeur dans une même variable.
var objet = document.getElementbyId("main"); // Un objet peut-être nimporte quel valeur. C'est une structure très utilisée et flexible. 


```


## Les variables 

```javascript 

var age = 20; // Variable basique, peut être utilité en local comme en global. 
let name = "Robin"; // La variable let permet de déclarer une variable qui ne peut être utilité que dans le bloc où elle a été déclaré. 
const sexe = "Homme"; // La variable const ne peut être modifié. Elle peut être appliqué en local comme en global. 
name.length // Affiche la taille de la variable name (5);

```

## Les tableaux 

```javascript 

const monTableau = ["Un", "Deux", "Trois", "Quatre", "Cinq", "Six"];
console.log(monTableau[0]); // Affiche le premier élement du tableau, ici "Un". 
console.log(monTableau[5]); // Affiche le 6 élement du tableau, qui est répértorié à l'index 5, ici "Six". 

monTableau.length; //Permet d'avoir le nombre d'index du tableau. 
monTableau.push("Sept"); // Ajoute "Sept à la fin du tableau. 




```

## Conditions : If, else

```javascript
const num1 = 50;
const num2 = 40;

if (num1 == num2) {  		//Si num1 est égal à num 2
	alert("Egalité");	// afficher "Egalité"
}else { 			//Sinon
	alert("Différent");	// afficher "Différent";
}


```

## Les événements

```javascript
dblclick="";	//Double-cliquer sur l'élément
mouseover="";	//Faire entrer le curseur sur l'élément
mouseout="";	//Faire sortir le curseur de l'élément
mousedown="";	//Appuyer (sans relâcher) sur le bouton gauche de la souris sur l'élément
mouseup="";	//Relâcher le bouton gauche de la souris sur l'élément
mousemove="";	//Faire déplacer le curseur sur l'élément
keydown="";	//Appuyer (sans relâcher) sur une touche de clavier sur l'élément
keyup="";	//Relâcher une touche de clavier sur l'élément
keypress="";	//Frapper (appuyer puis relâcher) une touche de clavier sur l'élément
focus="";	//« Cibler » l'élément
blur="";	//Annuler le « ciblage » de l'élément
change="";	//Changer la valeur d'un élément spécifique aux formulaires (input,checkbox, etc.)
input=""; 	//Taper un caractère dans un champ de texte (son support n'est pas complet sur tous les navigateurs)
select=""; 	//Sélectionner le contenu d'un champ de texte (input,textarea, etc.)


// Spécifique à l'élément <form>
submit; //Envoyer le formulaire
reset; //Réinitialiser le formulaire

//source : https://openclassrooms.com/courses/dynamisez-vos-sites-web-avec-javascript/les-evenements-24
```

## DOM 

```javascript
document.getElementById("idName"); // Permet de récupérer l'élément dont l'ID est spécifié, exemple <div id ="idName">.
document.getElementsByTagName('tagName'); // Permet de récupérer l'élément dont le tag est spécifié, exemple : <div>. 
document.getElementsByName('name'); // Permet de récupérer l'élément dont le name est spécifié, exemple : name="nom". 
document.querySelector(''); 
document.querySelectorAll('');


```

## Boucle while 

```javascript
var a = 0;
var b = 0; 

while (a < 3) { 	//A chaque recommencement de la boucle, la valeur a va s'incrémenter et s'ajouter à  b.  
	a++;		//Après la première itération : n = 1 et x = 1
	b += a;		//Après la deuxième itération : n = 2 et x = 3
}			//Après la troisième itération :	n = 3 et x = 6
			// Et la boucle s'arrête lorsque a n'est plus inférieur à 3. 

```

## Canvas 

```javascript 

beginPath(); //Initialisation  
moveTo(x,y); //Point de départ
lineTo(x,y); // Point d'arrivée
closePath(); //Clôture
strok(); | fill(); //Contour ou remplissage 


fill(); //remplir la forme
stroke(); //contour de la forme

fillStyle=""; // Permet de changer le style la forme.
strokeStyle=""; // Permet de changer le style du contour de la forme.


ctx.lineCap = "butt"; //Forme par défaut de type rectangulaire.
ctx.lineCap = "round"; //Forme avec les bords arrondis.
ctx.lineCap = "square"; //Forme avec un carré ajouté à chaque bords.

ctx.lineJoin ="round"; // Crée un angle avec les bords légérement arrondis.
ctx.lineJoin ="Bevel"; // Crée un angle avec les bords arrondis.
ctx.lineJoin = "miter";// Défaut, crée un angle sans style.


arc(x, y, rayon, startAngle, endAngle, sensAntiHoraire); 
// x, y --> coordonnées du centre
// rayon --> rayon du cercle. 
//startAngle souvent égale à 0.
// endAngle -->Utilisé Math.PI
// sensAntiHoraire --> true, false


//Exemple concrès de cercle.

ctx.arc(150,150,60,0,Math.PI,false);
ctx.arc(180,130,15,0,Math.PI*2,false);
							
```

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________


# Jquery


## Document Ready Element

```javascript

$(document).ready(function(){		   $(function(){
			       /*====*/   	
});					  });

```

## Les sélécteurs

```javascript

$('p'); // Séléctionne tout les paragraphes
$('.maClasse'); // Séléctionne les éléments avec la classe ".maClasse"
$('#monId'); // Séléctionne l'élément avec l'identifiant "#monId".
$('p .lien'); // Séléctionne tout les éléments ayant la classe ".lien" contenu dans le parent "p".
$('.lien + .visite'); //La sélection s'effectue sur les éléments ayant pour classe .visite,
et qui sont immédiatement précédés dun élément ayant pour classe .lien 
$('.lien ~ .visite');// Dans ce cas-là, ce sont tous les éléments .visite,
précédés immédiatement ou non par un élément .lien

$("p:first"); //Séléctionne le premier paragraphe trouvé
$("a:last"); // Séléctionne le dernier lien de la page
$("p:eq(2)"); //Séléctionne le 3eme paragraphe de la page (index 2).

$("p[id]"); //Séléctionne seulement les paragraphes ayant un identifiant

$("input[name=username]"); //Selectionne seulement l'élément du formulaire ayant comme nom "username"
$("input[name!=username]"); // Selectionne les éléments qui n'ont pas comme nom "username"

$("p:not(.rouge)"); // Selectinne tout les paragraphes execpté ceux ayant comme classe ".rouge"
$('input:not(.bleu, .vert)'); // Selectionne tout les éléments du formulaire excepté de ceux ayant comme classe ".bleu" et ".vert"

var $element = $('monElement'); //Sauvergarde la séléction dans une variable.

$('input:button'); // on sélectionne un input de type button
$('input:text'); // texte
$('input:file'); // fichier
$('input:checkbox'); // case à cocher
$('input:radio'); // bouton radio
$('input:submit'); //bouton d'envoi
:checked //vérifie qu'une case est cochée 
:disabled //cible les éléments désactivés 
:enabled //fait le contraire, il sélectionne les éléments activés

$('p').each(function(){
    
    $(this).html('Hello World !'); // $(this) représente le paragraphe courant

});


```

## Les événements

