# Susciter des réactions pour travailler un cas d'usage

Contexte : *Marguerite présente à Tom, pilote d'avion, son modèle de prédiction*

Scénario 1 :

    Marguerite (parle vite) : Donc voilà, j'ai élaboré un modèle XGBoost pour prédire le nombre de décès lors d'un crash d'avion. La profondeur maximale est de 7, le taux d'apprentissage est de 0.03, nous utilisons 500 arbres de décision, et les hyperparamètres ont été optimisés grâce à une validation croisée de type Grid Search. L'indice Gini atteint 0.75, avec une ROC AUC de 0.88.

    Tom (perplexe) : Excusez-moi, Marguerite, mais je comprends rien. Il fait quoi votre modèle, comment ça marche ce truc ?

    Marguerite (bégayant) : Eh bien, c'est... c'est que ces paramètres... ils sont essentiels pour que le modèle fonctionne bien avec... les données de météo, enfin...

Scénario 2 :

    Marguerite : Permettez-moi de vous montrer le graphique qui révèle les trois variables les plus influentes dans nos prédictions : le nombre de passager, la météo, et l'âge du pilote.

    Tom (intéressé) : C'est très clair. Je suis juste surpris que l'âge du conducteur soit si important. Pourriez-vous expliquer davantage ?

    Marguerite : Bien sûr. nous voyons que plus le conducteur est âgé, plus le nombre de décès est élevé. Cela peut s'expliquer par une meilleure formation des jeunes pilotes. 

    Tom : Je comprends mieux maintenant. En parlant de formation, elle est différente selon les pays, est ce que vous avez pris cela en compte ?

    Marguerite : Je n'y avais pas pensé, c'est une bonne idée !

> **A retenir :** Il est important de faire preuve de vulgariser et de faire preuve de pédagogie. En plus,
en faisant cela, le data scientist va pouvoir se nourrir des échanges pour améliorer son modèle