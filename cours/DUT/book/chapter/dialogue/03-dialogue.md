# Expliquer une prédiction, debug, ...
Contexte : *Une tempête est encours, Marguerite doit donner une estimation du nombre de sinistre sur une zone très précise*
Comme pour le dialogue 1, on peut reprendre les mêmes perso et le même décors, s'il y a une fenêtre, on peut ajouter des nuages pour montrer la tempête en cours

Scénario 1 : 

>**Marguerite** : Bon, les calculs sont terminés. Le modèle prévoit une centaine de sinistres.
>
>**Alex (étonné)** : Une centaine ? Ça me paraît super bas, il devrait y en avoir dix fois plus avec une tempête comme ça.
>
>**Marguerite  (agacée)** : Ah, c’est nul, franchement le machine learning, ça marche jamais comme on veut.


Scénario 2 : 

>**Marguerite** : Bon, les calculs sont terminés. Le modèle estime une centaine de sinistres.
>
>**Alex (étonné)** : Une centaine ? Ça paraît bas… on devrait en voir bien plus dans ces conditions.
>
>**Marguerite (réfléchissant)** : Hum, ok, je vais vérifier avec l’explicabilité pour comprendre ce qui limite la prédiction.

>**Marguerite (après analyse)** : Alors, la vitesse du vent est bien prise en compte, mais le modèle semble donner un poids faible à l’exposition du territoire, ce qui réduit la prédiction. Comment on avait récupéré cette donnée?

>**Alex** : On utilise un dataset en open data, il date de trois ans. Mais pour cette zone spécifique, l’exposition a probablement changé depuis. On devrait ajuster ça ou utiliser une source plus récente.
>
>**Marguerite** : Parfait, je vais mettre à jour la donnée, et on pourra faire un nouveau test.

> **A retenir :** Si le modèle restitue seulement un montant ou une probabilité d'appartenir à une classe, son usage est limité. Les utilisateurs ne peuvent pas bien comprendre la prédiction. Avoir l'explicabilité permet de valider la prédiction en connaissant l'influence des variables. Elle peut aussi être restituer à des interlocuteurs non techniques pour accompagner la prédiction et leur donner confiance dans les résultats
