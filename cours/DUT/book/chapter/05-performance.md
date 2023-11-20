# Evaluer les performances d'un modèle

```
🗨️(Le modèle est capable de bien prédire si les crashs ont plus de 100 décès)
👩‍🏫
Marguerite, Data Scientist
```

**Split en Train/Test :**

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

|                     | Prédiction < 100 décès | Prédiction > 100 décès  |
|---------------------|------------------------|-------------------------|
| Réalité < 100 décès |         300            |            50           |
| Réalité > 100 décès |         20             |            400          |
