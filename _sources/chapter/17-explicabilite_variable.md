# Explicabilité globale : Détails par variable

**Comment une variable influence la prédiction selon ses caractéristiques?**

```
🗨️(Peux tu me dire quelle est l'influence de la température dans la prédiction de la vitesse de vent ?)
```


```{figure} ../../../../assets/PDP_plot.png
---
width: 600px
name: PDP_plot

---
Partial Dependance Plot de Sklearn, Image par l'auteur
```


```{figure} ../../../../assets/contribution_plot.png
---
width: 600px
name: contribution_plot

---
Contribution_plot de Shapash, Image par l'auteur
```

Différentes méthodes de calculs : Partial dependence plot (PDP), Accumulated effect plots (ALE), selon les contributions locales.
