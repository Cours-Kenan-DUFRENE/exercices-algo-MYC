## objectif
Le code ci-dessous est proprement écrit et semble correct à première vue.
Mais il contient plusieurs erreurs de logique ou de comportement.

## code de départ : 

```js
function filterProducts(products, minPrice, maxPrice, sortBy) {
  const filtered = products.filter((product) => {
    return product.price > minPrice || product.price < maxPrice;
  });

  const sorted = filtered.sort((a, b) => {
    if (sortBy === "name") {
      return a.name > b.name;
    } else if (sortBy = "price") {
      return a.price - b.price;
    } else {
      console.log("Sort mode non reconnu:", sortBy);
      return 0;
    }
  });

  return sorted;
}

const catalog = [
  { name: "Sneakers", price: 80 },
  { name: "Hat", price: 25 },
  { name: "Watch", price: 120 },
  { name: "Socks", price: 10 }
];

const result = filterProducts(catalog, 20, 100, "price");
console.log("Résultat final :", result);

```

## ce que c'est sensé faire : 

- Prendre une liste de produits contenant un nom et un prix
- Filtrer les produits dont le prix est compris entre deux bornes min et max (inclus)
- Trier la liste filtrée selon un critère donné ("name" ou "price")
- Retourner une nouvelle liste triée, sans modifier la liste originale

~~ ce 
