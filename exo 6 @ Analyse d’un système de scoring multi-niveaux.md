
## objectif
Le code ci-dessous semble bien structuré et écrit… mais il produit des résultats incohérents dans certains cas.

## code de départ : 

```js
function calculateAverage(scores) {
  if (scores.length === 0) return 0;
  return scores.reduce((acc, val) => acc + val) / scores.length;
}

function evaluate(players) {
  const result = [];

  for (let player of players) {
    if (player.isActive === true) {
      const avg = calculateAverage(player.levelScores);
      result.push({ name: player.name, avg });
    }
  }

  result.sort((a, b) => b.avg - a.avg);

  for (let i = 0; i < result.length; i++) {
    result[i].rank = i + 1;
  }

  return players.map((p) => {
    const found = result.find((r) => r.name === p.name);
    return {
      name: p.name,
      rank: found ? found.rank : null,
      avg: found ? found.avg : null,
      active: p.isActive
    };
  });
}

const players = [
  { name: "Alice", isActive: true, levelScores: [50, 60, 80] },
  { name: "Bob", isActive: false, levelScores: [90, 95, 100] },
  { name: "Charlie", isActive: true, levelScores: [100] },
  { name: "Dylan", isActive: true, levelScores: [] },
];

console.log(evaluate(players));

```

## ce que c'est sensé faire : 

- Prendre une liste de joueurs, avec :
    + une série de scores par niveau (levelScores)
    + un statut (isActive)
- Calculer une moyenne des scores par joueur, uniquement s’il est actif
- Classer les joueurs selon leur moyenne
- Retourner un classement avec :
    + le nom
    + la moyenne
    + la position dans le classement final

~~ ce 
