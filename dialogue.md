## Susciter des réactions pour travailler un cas d'usage

Marie, Data Scientist, présente à Michel, vendeur de voiture, son modèle de la prévision de la demande de voitures électriques.

Scénario 1 :

    Marie (avec enthousiasme) : Donc voilà, j'ai élaboré un modèle XGBoost sophistiqué pour anticiper la demande de voitures électriques. La profondeur maximale est de 7, le taux d'apprentissage est de 0.03, nous utilisons 500 arbres de décision, et les hyperparamètres ont été optimisés grâce à une validation croisée de type Grid Search. L'indice Gini atteint 0.75, avec une ROC AUC de 0.88, ce qui signifie que notre modèle est particulièrement précis dans ses prévisions.

    Michel (perplexe) : Excusez-moi, Marie, mais ce jargon technique est difficile à suivre. Pouvez-vous expliquer en des termes plus simples pourquoi cette précision est importante pour nous ?

    Marie (bégayant) : Eh bien, c'est... c'est que ces paramètres... ils sont essentiels pour que le modèle fonctionne bien avec... les données de voitures électriques, enfin...

Scénario 2 :

    Marie : Permettez-moi de vous montrer le graphique qui révèle les trois variables les plus influentes dans nos prédictions de la demande de voitures électriques : la météo, le prix de l'électricité et la disponibilité des bornes de recharge.

    Michel (intéressé) : C'est plus clair maintenant. La météo, le prix de l'électricité, et la disponibilité des bornes de recharge sont les facteurs les plus importants. Pourtant, je me demande pourquoi la météo est si cruciale. Pourriez-vous expliquer davantage ?

    Marie : Bien sûr, Michel. La météo influe sur la demande de voitures électriques de plusieurs façons. Par exemple, les conditions météorologiques affectent la propension des gens à utiliser des véhicules électriques. Un temps ensoleillé peut stimuler la demande, tandis que la pluie ou la neige peut la réduire. Notre modèle prend en compte ces variations météorologiques pour anticiper précisément la demande.

    Michel : Je comprends mieux maintenant. En fonction des prévisions météorologiques, nous pourrions ajuster notre offre et nos opérations pour répondre à la demande changeante. Cela a du sens.

    Marie : Exactement, Michel ! La météo est un indicateur indirect qui a un impact sur la demande, et en comprenant cela, nous pouvons prendre des décisions plus informées pour mieux servir nos clients.

A retenir : Il est important de faire preuve de vulgariser et de faire preuve de pédagogie. En plus,
en faisant cela, le data scientist va pouvoir se nourrir des échanges pour améliorer son modèle


## transparence, confiance, acceptation sociale et maitrise de l'usage

Contexte : Une entreprise utilise un système d'IA pour trier les candidatures

Scénario 1 : 

    Candidat : J'ai postulé pour un poste, mais ma candidature a été rejetée sans explication. Pourquoi ?

    Responsable des Ressources Humaines : Désolé, notre système a pris cette décision en fonction des données que vous avez fournies, mais nous ne pouvons pas vous expliquer pourquoi. C'est une décision automatisée.

    Candidat : Cela me semble injuste. Comment puis-je être sûr que la décision était basée sur des critères équitables ?

Scénario 2 : 

    Candidat : J'ai postulé pour le poste de développeur de logiciels Python, mais ma candidature a été rejetée. Pouvez-vous m'expliquer pourquoi ?

    Responsable des Ressources Humaines (RH) : Bien sûr, John. Notre système d'IA a examiné plusieurs critères, y compris le nombre d'années d'expérience, la correspondance de vos compétences techniques avec l'offre d'emploi, et votre formation en informatique. Dans votre cas, vous avez 2 ans d'expérience en développement, ce qui est solide, mais d'autres candidats avaient plus de 6 ans d'expérience spécifiquement en développement Python.

    Candidat : Je comprends. Est-ce qu'il y avait d'autres facteurs qui ont influencé la décision ?

    Responsable des Ressources Humaines (RH) : Notre système a également noté un léger manque d'expérience en Python dans vos précédents emplois, par rapport aux autres candidats. Cela a pesé dans la balance en faveur des candidats ayant une expérience plus approfondie dans Python.

    Candidat : Merci pour les détails. Cela m'aide vraiment à comprendre la décision. Je vais travailler sur mes compétences en Python et continuer ma recherche.

A retenir : L'explicabilité peut aider à donner confiance aux utilisateurs de l'IA. Elle permet également d'être transparent sur 
la prédiction effectué. Cela peut permettre de favoriser l'acceptation l'usage de l'IA. 
A noter qu'il ne suffit pas de l'explicabilité, il faut aussi que l'IA soit utile pour la société, éthique, transparente,..
L'utilisateur du produit d'IA est plus en maitrise de son usage si on complémente la prédiction avec de l'explicabilité. Dans ce cadre, il est en maitrise de faire usage ou non du retour de la prédiction

## itérer et améliorer l'aprentissage, analyser les incohérences, détecter les biais, 
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




- comme produit d'IA
Dialogue scénario 1 : une start up qui propose de prédire le nombre de décès pour anticiper le nombre de cerceuil à prévoir lors de la venue des secours
scénario 2 :  une explication du nombre de décès

- à des fins d'audit
Pour fournir la possibilité d'auditer les choix de prédiction d'un  modèle
- la réglementation
l'IA act  : notion de transparence et explicabilité et traçabilité
projections : adoption du texte en 2023 et application pleine en 2026.
notion de niveaux de risques du système d'IA
