# Itérer et améliorer l'aprentissage, analyser les incohérences, détecter les biais, 
Contexte : *Marguerite parle de son modèle à son camarade Data scientist Alex*

Scénario 1 : 

    Marguerite (enthousiaste) : Hey, mec, j'ai entrainé mon modèle, et j'ai un AUC de 0.91. 

    Alex (désintéressé): ah, ba c'est cool dis donc.    

Scénario 2 : 

    Marguerite (enthousiaste) : Hey, mec, j'ai entrainé mon modèle, j'ai un AUC de 0.91. Mon top 3 de variables, c'est le nombre de passager, 
    l'âge du pilote, et l'heure du vol. Viens voir mon explicabilité. 

    Alex (intéressé): Ah ouais, à quelle heure ça a le plus d'impact. Tiens, c'est intéressant que les plus gros accident ont lieux à 6h du matin. Comment
    tu as géré les fuseaux horaires dans tes données ?

    Marguerite : Ah mince, j'ai pas fais attention à ça, je vais vérifier plus tard. 

    Alex : Est ce que tu as essayé de prendre en compte les conditions météos, je connais une base de données avec laquelle tu pourrais
    ajouter des infos

    Marguerite : Ah oui cool, merci, je pourrai essayer de les rajouter. Par contre le modèle se trompe sur certains crash, j'ai des exemples à te montrer. Par exemple, sur ce crash.

    Alex : ah c'est bizarre, tu as récupéré l'âge du pilote à partir de quelle base de données ? Selon les bases, l'informations est plus ou moins fiables

    Marguerite : Ah ok, je vais vérifier cette données alors.

> **A retenir :** A partir de l'explicabilité, il est possible d'itérer sur l'apprentissage du modèle. Ajouter des variables, 
supprimer des variables non nécessaires, vérifier la qualité des données, debugger, modifer la transofrmation des variables explicatives.
Et donc avoir un modèle d'une meilleure qualité et plus performant.