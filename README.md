# Atelier "Apprentissage automatique pour la classification textuelle"
## ANF CNRS "Exploration documentaire" 2021

Cet atelier permet d'explorer des tâches de classification automatique non supervisée (k-moyennes et cartes auto-organisées) ou supervisée (classification bayésienne, arbres de décision, réseaux de neurones profonds et plongements lexicaux). Les données sont d'une part les méta-données de documents issus d'ISTEX concernant le mot clé "covid" (catégorisation en domaines à partir des résumés puis partitionnement) et une collection de critiques IMDB de films pour l'analyse de sentiment.
Les environnements sont Jupyter Notebook et Weka. Le langage est Python.

Pour réaliser les exemples de l'atelier, vous devez : 

Pour une exécution du code Python dans l'environnement Google Colab : 
  - disposer d'un compte Google, accéder à votre Google Drive http://drive.google.com/
  - ouvrir les deux Notebooks (.ipynb) disponibles ici dans l'environnement Google Colab : cliquer sur le nom du carnet puis sur l'icône Colab présent en haut de la zone ouverte. NB : cela créera un dossier ColabNotebooks dans votre GoogleDrive si vous n'en avez pas déjà.
- déposer dans votre Google Drive / ColabNotebooks le fichier CorpusCovid.csv présent ici ainsi que les critiques de films (voir plus bas)

L'alternative consiste à utiliser Python sur votre propre ordinateur. Pour cela je vous conseille fortement d'utiliser Jupyter Notebook (https://jupyter.org) via un gestionnaire d'environnements (par ex. https://anaconda.org) ou un IDE tel que PyCharm (https://www.jetbrains.com/fr-fr/pycharm/).

Dans tous les cas, vous devez : 
  - télécharger le fichier http://ai.stanford.edu/~amaas/papers/data/sentiment/ qui contient les critiques de films utilisées pour l'analyse de sentiment. Il s'agit d'un corpus bien connu, autour duquel beaucoup d'expérimentations sont réalisées (voir par exemple https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/code). Ces données sont décrites dans Andrew L. Maas, Raymond E. Daly, Peter T. Pham, Dan Huang, Andrew Y. Ng, and Christopher Potts. (2011). Learning Word Vectors for Sentiment Analysis. The 49th Annual Meeting of the Association for Computational Linguistics (ACL 2011) - https://ai.stanford.edu/~amaas/papers/wvSent_acl2011.pdf 
  - installer l'environnement Weka : https://www.cs.waikato.ac.nz/~ml/weka/

ps : les diapositives qui reprennent les exemples sont ici : https://drive.google.com/file/d/1iDkoNf5Oc6emFU1Jm78Bb4A7YP7HcVDm/view?usp=sharing

Pour toute question : patrice.bellot@univ-amu.fr

## Présentation des 2 carnets proposés

- Le carnet IMDB.
  - Il contient le code Python nécessaire pour effectuer une analyse de sentiment de critiques de films de type "classification binaire de la polarité de la critique". Appliquée à un corpus de 50 000 critiques en anglais de films issues de la plateforme IMDB, la tâche consiste à apprendre un modèle numérique qui détermine automatiquement la polarité de la critique : polarité négative versus polarité positive. L'approche n'utilise que très peu de ressources linguistiques puisque seule une liste de "mots outils" est exploitée. Il est ainsi très facile de reconstruire un modèle similaire pour le français. 
  - Les méthodes appliquées sont la classification bayésienne naïve (modèles dits "sacs de mots" où les mots sont considérés indépendamment les uns des autres) puis différentes réseaux de neurones profonds (deep learning). Il est intéressant de relever l'écart de performance entre les solutions et de le mettre en regard avec les temps de calcul nécessaires à l'apprentissage des modèles. On voit dans le code à quel point les architectures neuronales sont configurables.
  - Le code s'appuie sur les modules Python Pandas (manipulation des données), SciKit Learn (classification bayésienne), Keras/Tensorflow (réseaux de neurones).

- Le carnet ClassificationMetaISTEX.
  - Il contient le code Python pour d'une part mettre en forme les données issues de la plateforme ISTEX mais aussi pour réaliser différentes classification non supervisée (partitionnement) avec les méthodes des k-moyennes (kMeans) et construire des cartes auto-organisées (Self Organized Maps SOM). 
  - Les modules Python utilisés sont Pandas (manipulation des données), SciKit Learn (kMeans), somoclu (cartes auto-organisées). 
  - Les données ainsi mises en forme dans un fichier .CSV peuvent être récupérées dans l'environnement Weka que nous utilisons pour apprendre des modèles de classification (approche bayésienne et arbres de décision) en catégories scientifiques à partir des résumés des articles du corpus. Il est bien sûr
 possible de construire des modèles équivalents en restant dans l'environnement Python. 
