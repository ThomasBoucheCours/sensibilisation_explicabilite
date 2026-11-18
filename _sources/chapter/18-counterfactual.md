# A base de contre exemples

**Quelles modifications dans les variables peuvent entraîner un changement de prédiction ?**

> 🗨️ Peux-tu m'indiquer les conditions qui auraient dû être réunies
> pour augmenter la vitesse de vent ?

L'idée est de modifier des paramètres du dataset pour changer la prédiction.

```{figure} ../../../../assets/dice_example.png
---
width: 750px
name: dice_example

---
Exemple explicabilité à base de contre exemples, de la librairie [DICE](https://github.com/interpretml/DiCE)
```

**Ce que l'on cherche ici :** comprendre dans quelles conditions une prédiction aurait pu être différente pour un cas donné.

**Ce que l'on obtient :** des contre-exemples plausibles qui montrent les changements associés à une autre prédiction.

**Le message à retenir :** un counterfactual ne sert pas seulement à expliquer le passé, il sert à rendre la décision lisible, en montrant ce qui pèse dans la situation actuelle, ce qui aurait pu changer le résultat, et la distance entre la situation observée et une situation plus favorable.

> 🗨️ Quel scénario concret permet de faire passer ce répondant
> d'un profil "à risque" à "moins à risque",
> avec le meilleur compromis impact/coût ?
