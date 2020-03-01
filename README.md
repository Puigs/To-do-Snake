Bonjour à tous!

Aujourd'hui on va tenté de créer un jeu Snake en js en trois heures.
Je vous guiderai pour vos premiers pas mais ensuite vous allez devoir le finir seul ;)
Tout d'abord je vous laisse clone le repo afin d'obtenir deux fichiers, un html et un js vous permettant de commencer ce défi avec une bonne base ;)

Si vous ouvrez le fichier html dans votre browser favori, vous devrier voir afficher un carré gris, il s'agit de votre zone de jeu, votre canvas.
Qu'es qu'un canvas? Man google les gars ;)

Maintenant vous devriez commencer par créer un component, pour se faire je vous laisse intégrer ce code à votre projet :

```function component(width, height, color, x, y) {
  this.width = width;
  this.height = height;
  this.x = x;
  this.y = y;
  ctx = myGameArea.context;
  ctx.fillStyle = color;
  ctx.fillRect(this.x, this.y, this.width, this.height);
}```

