# Evaluer les performances d'un modèle

```
🗨️(Le modèle est capable de bien prédire les vitesses de vents supérieurs à 100km/h)
👩‍🏫
Data Scientist
```

**Indépendance entre les données d’entraînement et de test :**

| Variables        | split     |
|------------------|-----------|
| x₁, x₂, ...      | Train     |
| ...              | Test      |
| ...              | Test      |
| ...              | ...       |
| ...              | ...       |
| ...              | ...       |
| xn₁, xn₂, ...    | Train     |

<br /> 
<br /> 

**Evaluation sur les données de Test :**

|                              | Prédiction wind_speed < 100km/h | Prédiction wind_speed > 100km/h |
|------------------------------|---------------------------------|---------------------------------|
| Réalité wind_speed < 100km/h |         3000                    |            500                  |
| Réalité wind_speed > 100km/h |         20                      |            40                   |
