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

![Machine_learning](Machine_learning.png)
--> cité le livre christoph M


Périmètre :  apprentissage supervisé, données tabulaires
Examples Classification et Régression
## Evaluer les performances d'un modèle
- présentation

- à quoi ça sert ?

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

# Les différents types d'explicabilité

méthodes agnostiques  --> avantages, utilisables sur tous les modèles et comparables

## Explicabilité globale
### feature importance
Quelles sont les variables explicatives qui ont le plus de poids dans la prédiction ?

Exemple de graphique

Différentes méthodes de calculs : des méthodes intégrées aux fonctionnalités du modèle (par exemple gini importance pour sklearn), Permutation based feature impotance, la somme des contributions locales 

### feature effect plot
Comment une variable influence la prédiction selon ses caractéristiques?

Exemples de graphiques

Différentes méthodes de calculs : partial dependence plot (PDP), Accumulated effect plots (ALE), selon les contributions locales

## Explicablité locale
Quelle est l'influcence de chaque variable sur une prédiction ?

exemple : image shap github

Différentes méthodes de calculs : Shapley Values, Lime

## Autres méthodes
- A base de contre exemples

Image Dice

## les limites de certaines méthodes
corrélations entre les variables
--> exemples de méthodes et graphiques


# Comment ça s'applique ?


# Comment sélectionner la population à évaluer



# Evaluation de l'explicabilité
Comment évaluer la qualité d'une explicabilité ?
- le facteur humain
- un proxy qui permet de valider
- Des indicateurs



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
- [plotly](https://github.com/plotly/plotly.py)
- [dash](https://github.com/plotly/dash)


# A faire
préciser à qui s'adresse la présentation, le public et le format, le périmètre