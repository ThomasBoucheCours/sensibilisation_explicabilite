# Susciter des réactions pour travailler un cas d'usage

Contexte : *Marguerite présente à des "non experts de la données" son modèle*
cadre : Dans une salle de réunion, un data scientist qui présente ses résultats sur un grand écran
persos : un des datascientists du dialogue 1, on peut avoir 3-4 personnes qui assitent à a présentation, plus agé entre 40 et 60 ans
Scénario 1 :

>**Marguerite (parle vite)** : Donc voilà, j'ai élaboré un modèle XGBoost pour prédire le nombre de sinistres tempêtes au cours d'un évènement climatique. La profondeur maximale est de 7, le taux d'apprentissage est de 0.03, nous utilisons 500 arbres de décision, et les hyperparamètres ont été optimisés grâce à une validation croisée de type Grid Search. L'indice Gini atteint 0.75, avec une ROC AUC de 0.88.
>
>**Interlocuteur métier(perplexe)** : Désolé, mais je comprends rien. Concrètement, il fait quoi, ce modèle ? Et tous ces chiffres, ça signifie quoi ?
>
>**Marguerite (bégayant, perdue)** : Eh bien, c'est... c'est que ces paramètres... ils sont essentiels pour que le modèle fonctionne bien avec... les données de météo, enfin...
>**Interlocuteur métier(désabusé)** : Bon, tant que ça marche...
>

Scénario 2 :

>**Marguerite** : Nous avons construis un modèle de prédiction des sinistres associés à une tempête au cours d'un évènement climatique. Pour vus donner quelques explications, les 3 variables les plus influentes sont: La vitesse de vent, la direction du vent et la vulnérabilité du territoire.
>
>**Interlocuteur métier (intéressé)** : C’est clair ! Est-ce que vous avez pris en compte le relief ? Par expérience, une tempête frappe >différemment au bord de la mer que dans les terres.
>
>**Marguerite** : Très bon point ! On a inclus la vulnérabilité du territoire, mais pas le relief. Merci pour la suggestion, on pourrait >l’ajouter pour affiner les prédictions !
>
>**Marguerite** : Par rapport à la vitesse de vent, on peut voir sur ce graphique que le modèle prédit des sinistres qu'à partir de 100km/h et que le risque est multiplié par 10 au delà de 140km/h
>
>**Interlocuteur métier (intéressé)** : C’est parlant, on retrouve ce qu’on constate souvent sur le terrain. Merci !
>
> **A retenir :** Il est important de vulgariser et de faire preuve de pédagogie. De plus, le data scientist va pouvoir se nourrir des échanges pour améliorer son modèle.