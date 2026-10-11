# Explicablité locale

**Quelle est l'influence de chaque variable sur la prédiction d'un individu ?**

```
🗨️(Peux tu me dire pourquoi ce vent est de x km/h ?)
```

## Shapley Values
Une prédiction peut s'expliquer en considérant que chaque valeur des données d'entrée est un « joueur » dans un jeu où la prédiction correspond au gain. Les Shapley Values – une méthode issue de la théorie des jeux – nous indiquent comment répartir équitablement ce « gain » entre les données d'entrée.


```{figure} ../../../../assets/shap_exemple.png
---
width: 750px
name: shap_exemple

---
contribution locale de shap, Image par l'auteur
```

```{figure} ../../../../assets/shapash_local_plot.png
---
width: 750px
name: shapash_local_plot

---
contribution locale de Shapash, Image par l'auteur
```