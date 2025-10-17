
## Objectif :

Analyser un code difficile à lire, mal structuré et confus, puis le réécrire proprement en suivant les principes vus en cours :
+ lisibilité
+ noms explicites
+ découpage logique
+ suppression des répétitions

## code de départ

```js
function r(users, s) {
  let w = [];
  for (let i = 0; i < users.length; i++) {
    let u = users[i];
    let sum = 0;
    for (let j = 0; j < u.s.length; j++) {
      if (u.s[j] >= s) {
        sum += u.s[j];
      }
    }
    if (sum > 0) {
      w.push({ n: u.n, t: sum });
    }
  }
  w.sort(function(a, b) {
    return b.t - a.t;
  });
  let top = w[0] ? w[0].n : null;
  console.log("Top:", top);
}
```

## exemple d'appel : 

```js
p([
  { p: 50, c: "tech" },
  { p: 120, c: "clothes" },
  { p: 300, c: "tech" },
  { p: 90, c: "home" },
  { p: 500, c: "tech" },
], 100);
```

## ce que fais le code : 
- On ne sait pas car ce n'est pas nous qui l'avons écrit :(

## Consignes :

- Renommer la fonction et les variables de manière explicite
- Séparer les responsabilités dans des fonctions dédiées (ex: calcul du total, tri)
- Ajouter des commentaires utiles
- Vérifier que le code est lisible même sans indentation colorée

- Bonus : proposer une version qui retourne le résultat au lieu de l'afficher en console



- Affiche ces deux résultats dans la console
