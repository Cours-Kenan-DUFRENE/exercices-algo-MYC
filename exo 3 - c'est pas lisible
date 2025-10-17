## Objectif :

Analyser un code difficile à lire, mal structuré et confus, puis le réécrire proprement en suivant les principes vus en cours :
+ lisibilité
+ noms explicites
+ découpage logique
+ suppression des répétitions

## code de départ

```js
function p(d, t) {
  let s = 0, c = 0, m = {};
  for (let i = 0; i < d.length; i++) {
    let it = d[i];
    if (it.p > t) {
      s += it.p;
      c++;
      if (!m[it.c]) {
        m[it.c] = 1;
      } else {
        m[it.c]++;
      }
    }
  }
  let a = s / c;
  let mc = null, mv = 0;
  for (let k in m) {
    if (m[k] > mv) {
      mv = m[k];
      mc = k;
    }
  }
  console.log("avg:", a, "top:", mc);
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
- Parcourt un tableau d’achats (d)
- Ne garde que les produits dont le prix p dépasse un certain seuil t
- Calcule la moyenne de prix de ces produits
- Identifie la catégorie la plus fréquente parmi eux
- Affiche ces deux résultats dans la console
