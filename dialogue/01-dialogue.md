# Itérer et améliorer l’apprentissage, analyser les incohérences, détecter les biais,  
Contexte : *Marguerite parle de son modèle à son camarade Alex, également data scientist*
cadre : Dans un open space ou bureau, 2 camarades data scientists sont chacun sur leur pc, Marguerite interpelle sont camarade Alex
persos : des datascientists, la trentaine,

Scénario 1 : 

> **Marguerite (enthousiaste)** : Hey, mec, j'ai entraîné mon modèle, et j'ai un AUC de 0.98 !!
>
> **Alex (désintéressé, sans lever les yeux de l’écran)**: ah, ba c'est cool dis donc.

Scénario 2 : 

>**Marguerite (enthousiaste)** : Hey, mec, j'ai entraîné mon modèle, j'ai un AUC de 0.98 !! Je viens de calculer l'explicabilité du modèle, regarde.
>
>**Alex (intéressé)**: Wow, c’est élevé ! Mais attends, la première variable explique presque tout à elle seule… ça semble être un proxy direct. Est-ce que tu l’auras en production ?
>
>**Marguerite (réalisant le problème)** : Oh mince, non, celle-là, elle ne sera pas disponible pour la prédiction… Je vais la retirer et ré-entraîner le modèle.
>
>**Alex** : Tes autres variables, elles sont intéressantes. Tu les as construites comment ? Elles viennent de quelles sources ?

>**A retenir** : A partir de l’explicabilité, il est possible d’itérer sur l’apprentissage du modèle. Ajouter des variables, supprimer des variables non nécessaires, vérifier la qualité des données, debugger, modifier la transformation des variables explicatives. Et donc avoir un modèle d’une meilleure qualité et plus performant.