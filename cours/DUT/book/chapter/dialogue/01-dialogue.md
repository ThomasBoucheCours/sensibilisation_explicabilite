# Itérer et améliorer l'aprentissage, analyser les incohérences, détecter les biais, 
Contexte : Sarah a entrainé un modèle de prédiction du risque d'accident automobile et en parle à son
camarade dadat scientist Alex

Scénario 1 : 

    Sarah (enthousiaste) : Hey, mec, j'ai entrainé mon modèle, et j'ai un AUC de 0.91. 

    Alex (désintéressé): ah, ba c'est cool dis donc.    

Scénario 2 : 

    Sarah (enthousiaste) : Hey, mec, j'ai entrainé mon modèle, j'ai un AUC de 0.91. Mon top 3 de variables, c'est le genre, 
    l'âge du conducteur, et l'heure de la conduite. Viens voir mon explicabilité. 

    Alex (intéressé): Montre moi la courbe selon l'âge. Tiens, c'est intéressant que les moins de 25 ans ont plus d'accident que les
    les plus de 80 ans. ont voit que les accidents ont lieux la nuit, ça doit être liée à l'alcool.

    Sarah : Ah oui surement, d'ailleurs, j'ai une description textuelle des circonstances de l'accident, avec des exemples
    qui parle de la consommation d'alcool, je pourrai créer une variable à partir de cela.
    Tu as d'autres idées de variables à ajouter ?

    Alex : Est ce que tu as essayé de prendre en compte les conditions météos, je connais une base de données avec laquelle tu pourrais
    ajouter des infos

    Sarah : Ah oui cool, merci, je pourrai essayer de les rajouter. Par contre le modèle se trompe sur certains indvidus, j'ai des exemples à te montrer. Par exemple, sur cet individu.

    Alex : ah c'est bizarre, tu as récupéré l'âge à partir de quelle base de données ? Selon les bases, l'informations est plus ou moins fiables

    Sarah : Ah ok, je vais vérifier cette données alors.

A retenir : A partir de l'explicabilité, il est possible d'itérer sur l'apprentissage du modèle. Ajouter des variables, 
supprimer des variables non nécessaires, vérifier la qualité des données, debugger, modifer la transofrmation des variables explicatives.
Et donc avoir un modèle d'une meilleure qualité et plus performant