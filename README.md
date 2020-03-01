Bonjour à tous!

Aujourd'hui on va tenter de créer un jeu Snake en js en trois heures.
Je vous guiderai pour vos premiers pas mais ensuite vous allez devoir le finir seul ;)
Tout d'abord je vous laisse clone le repo afin d'obtenir deux fichiers, un html et un js vous permettant de commencer ce défi avec une bonne base ;)

Si vous ouvrez le fichier html dans votre browser favori, vous devrier voir afficher un carré gris, il s'agit de votre zone de jeu, votre canvas.
Qu'es qu'un canvas? Man google les gars ;)

Maintenant vous devriez commencer par créer un component, pour se faire je vous laisse intégrer ce code à votre projet :
```js 
function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y;
  ctx = myGameArea.context;
  ctx.fillStyle = color;
  ctx.fillRect(this.x, this.y, this.width, this.height);
}
```
Allez je vais vous guidez encore un peu, pour faire un jeu ça peut être sympa d'update votre zone de jeu non?
Essayez d'ajouter à votre méthode start de l'objet myGameArea la ligne suivante :
```
    this.interval = setInterval(updateGameArea, 20);
```

Ensuite créer une méthode clear à l'objet myGameArea:
```
clear : function() {
    this.context.clearRect(0, 0, this.canvas.width, this.canvas.height);
  }
```

Maintenant il faut ajouter la fonction suivante à notre js : 
```
function updateGameArea() {
  myGameArea.clear();
  myGamePiece.update();
}
```

Et pour finir vous devez modifier votre component avec le code suivant :
```
this.update = function(){
    ctx = myGameArea.context;
    ctx.fillStyle = color;
    ctx.fillRect(this.x, this.y, this.width, this.height);
  }
```

Pour vérifiez que tout fonctionne faite déplacer votre component en ajoutant la ligne suivante à votre fonction updateGameArea : 
```
myGamePiece.x += 1;
```

Pour la suite à vous de créer le jeu! 
Si vous avez des questions hésitez pas à venir nous voir ;)
