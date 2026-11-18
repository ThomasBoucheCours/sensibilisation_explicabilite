# Explicabilité globale : Feature importance

**Quelles sont les variables explicatives qui ont le plus de poids en moyenne dans la prédiction ?**

```
🗨️(Peux tu me dire quels sont les critères qui ont le plus d'impacts pour prédire la vitesse de vent?)
```

```{figure} ../../../../assets/feature_importance.png
---
width: 750px
name: feature_importance

---
Feature importance de Shapash, Image par l'auteur
```

Différentes méthodes de calculs : des méthodes intégrées aux fonctionnalités du modèle (par exemple Gini importance pour sklearn), Permutation based feature importance, la somme des contributions locales.

Dans le cas de SHAP, l'importance globale d'une variable $j$ est généralement calculée comme la moyenne des contributions absolues sur l'ensemble des observations :

$$
\mathrm{FI}_j = \frac{1}{n}\sum_{i=1}^{n}\left|\phi_j^{(i)}\right|
$$

où $\phi_j^{(i)}$ est la valeur de Shapley (SHAP) de la variable $j$ pour l'observation $i$, et $n$ le nombre d'observations.

Une version normalisée (en pourcentage) peut ensuite être obtenue via :

$$
\mathrm{FI}^{\%}_j = \frac{\mathrm{FI}_j}{\sum_{k=1}^{p}\mathrm{FI}_k}
$$

avec $p$ le nombre total de variables.

---

**Focus SHAPASH : importance globale, semi-locale et locale**

SHAPASH reprend l'idée de base de SHAP (agrégation des contributions locales $\left|\phi_j^{(i)}\right|$), puis propose des métriques qui accentuent progressivement les contributions très fortes observées sur une partie des individus.

Pour une variable $j$, on peut écrire une famille de scores :

$$
\mathrm{FI}_j^{(q)} = \frac{1}{n}\sum_{i=1}^{n}\left|\phi_j^{(i)}\right|^q
$$

avec :

- $q=1$ : importance globale (moyenne classique des $|\phi|$)
- $q=3$ : importance semi-locale (met davantage en avant les contributions élevées)
- $q=7$ : importance locale (met fortement en avant les cas où la variable a un impact très important)

Plus $q$ augmente, plus le score devient sensible aux grandes valeurs de Shapley. Cela permet de faire ressortir des variables qui ne sont pas forcément dominantes en moyenne globale, mais qui peuvent être déterminantes sur des sous-populations.

```{figure} ../../../../assets/feature_importance_local.png
---
width: 850px
name: feature_importance_local

---
Feature importance SHAPASH avec métriques globale, semi-locale et locale
```