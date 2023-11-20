# Sommaire
- Introduction
- Qu'est ce que l'explicabilité
- Pourquoi avoir de l'explicabilité
- Les différents types d'explicabilité
- Comment ça s'applique ?
- Evaluation de l'explicabilité
- Packages Python


# Introduction

Présentateur : Thomas Bouché, Data scientist à la Maif depuis 2019. Contributeur à la librairie Shapash, 
open sourcé par la Maif et qui a pour but de rendre les modèles de machine learning compréhensible pour tous.

## les objectifs de la sensibilisation
- Connaitre les différentes explicabilités à présenter avec son modèle de machine learning
- être curieux sur le fonctionnement d'un modèle de machine learning
- Connaitre les différents usages et avantages de l'explicabilité


## Qu'est qu'un modèle de machine de machine learning

Définition de la CNIL :  

"L’apprentissage automatique (machine learning en anglais) est un champ d’étude de l’intelligence artificielle qui vise à donner aux machines la capacité d’« apprendre » à partir de données, via des modèles mathématiques. Plus précisément, il s’agit du procédé par lequel les informations pertinentes sont tirées d’un ensemble de données d’entraînement.

Le but de cette phase est l’obtention des paramètres d’un modèle qui atteindront les meilleures performances, notamment lors de la réalisation de la tâche attribuée au modèle. Une fois l’apprentissage réalisé, le modèle pourra ensuite être déployé en production."

![Machine_learning](./assets/Machine_learning.png)
--> cité le livre christoph M


Périmètre :  apprentissage supervisé, données tabulaires
Examples Classification et Régression

Liste des modèles : 


## Exemple pour le cours



## Evaluer les performances d'un modèle
- présentation
A partir d'un échantillon de données indépendant de celui qui a servit à l'apprentissage du modèle, 
on compare les prédictions du modèle avec la réalité. 
ceci permet d'obenit des indicateurs de performance du modèle.

Exemple pour un modèle de classification :
![Matrice de confusion](./assets/confusion_matrix.png)

# Qu'est ce que l'explicabilité
Définition de la CNIL de l'explicabilité :
"Dans le domaine de l'intelligence artificielle, l’explicabilité est la capacité de mettre en relation et de rendre compréhensible les éléments pris en compte par le système d’IA pour la production d’un résultat.

Il peut s’agir, par exemple, des variables d’entrée et de leurs conséquences sur la prévision d’un score, et ainsi sur la décision.

Les explications doivent être adaptées au niveau de compréhension de la personne auxquelles elles sont destinées."


Est ce que le modèle est interprétable par design ?
régression linéaire, régression logistique, arbre de décision, GLM, ...



# Pourquoi avoir de l'explicabilité
Périmètre : principalement les modèles non directement interprétables

## Quelles utilités ?
- susciter des réactions pour travailler un cas d'usage
- la transparence
- Donner confiance
Pour un utilisateur, comprendre comment le modèle fonctionne, comprendre les circonstances de la prédiction du modèle et pouvoir 
avoir confiance en la prédiction
- itérer et améliorer l'aprentissage
Pour un data scientist, comprendre comment le modèle fonctionne, pour le débuger ou l'améliorer. Voir les variables qui fonctionne bien ou non et comprendre pourquoi
- analyser les incohérences
- détecter les biais
- pour les utilisateurs finaux, être en maitrise de la compréhension de la prédiction
pour un utilisateur, comment une prédiction a été effectuée, et voir si cette prédiction est cohérente et avoir des pistes d'améliorations de 
la prédiction
- comme produit d'IA
- favorise l'acceptation sociale de l'ia
Pour la société, comprendre les forces et les limites du fonctionnement des modèles et dépasser "la peur de l'inconnu"
- pour du débuggage
- à des fins d'audit
- la réglementation
Pour fournir la possibilité d'auditer les choix de prédiction d'un  modèle

A qui s'adresse :
- aux data scientists
- aux utilisateurs finaux
- aux décideurs
- aux instances de réglementations
--> ajouter les apports pour chacun ?

# Les différents types d'explicabilité

explicabilité agnostiques au modèle :
- être applicable aux différents modèles
- s'appuie sur les données d'entrées et la prédiction
- permet de comparer les résultats entre modèles et méthodes d'explicabilités

## Explicabilité globale
### feature importance
Quelles sont les variables explicatives qui ont le plus de poids dans la prédiction ?

![feature importance](./assets/feature_importance.png)

Différentes méthodes de calculs : des méthodes intégrées aux fonctionnalités du modèle (par exemple gini importance pour sklearn), Permutation based feature impotance, la somme des contributions locales 

### feature effect plot
Comment une variable influence la prédiction selon ses caractéristiques?

![partial dependence plot](./assets/PDP_plot.png)
from molnar

Différentes méthodes de calculs : partial dependence plot (PDP), Accumulated effect plots (ALE), selon les contributions locales

## Explicablité locale
Quelle est l'influcence de chaque variable sur une prédiction ?

![Exemple Shap](./assets/shap_example.png)

Différentes méthodes de calculs : Shapley Values, Lime

## Autres méthodes
- A base de contre exemples

![Exemple counterfactual](./assets/dice_example.png)

## les limites de certaines méthodes
corrélations entre les variables
--> exemples de méthodes et graphiques

causal interpretation

## choix d'un modèle
performance versus explicabilité

compromis entre explicabilité et performance du modèle
+ simplicité de mise en place
+ simplicité de maintien dans le temps
+ harmonisation des pratiques


# Comment ça s'applique ?

![usage_explicabilite](./assets/usage_explicabilite.png)


# Comment sélectionner la population à évaluer
- Les individus avec des erreurs de prédictions
A la frontière ou loin de la frontière

Exemple avec Shapash


- Des individus exemples
Propos sur le clustering

- En filtrant par variables 
Présentes ou non dans le modèle



# Evaluation de l'explicabilité
Comment évaluer la qualité d'une explicabilité ?
- le facteur humain
- un proxy qui permet de valider
- Des indicateurs

# Un petit mot sur l'image et le texte


# Citations

- Molnar, C. (2022). Interpretable Machine Learning:
A Guide for Making Black Box Models Explainable (2nd ed.).
[christophm.github.io/interpretable-ml-book/](https://christophm.github.io/interpretable-ml-book/)

- Explainable Artificial Intelligence, From Simple Predictors to Complex Generative Models, Spring 2023, Harvard University.
[interpretable-ml-class.github.io](https://interpretable-ml-class.github.io/)

- https://www.cnil.fr/fr/glossaire

# Packages Python
- [scikit-learn](https://github.com/scikit-learn/scikit-learn)
- [shap](https://github.com/shap/shap)
- [shapash](https://github.com/MAIF/shapash)
- [DiCE](https://github.com/interpretml/DiCE)
- [plotly](https://github.com/plotly/plotly.py)
- [dash](https://github.com/plotly/dash)


# A faire
préciser à qui s'adresse la présentation, le public et le format, le périmètre