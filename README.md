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
- télécharger le fichier http://ai.stanford.edu/~amaas/papers/data/sentiment/ qui contient les critiques de films utilisées pour l'analyse de sentiment 
- installer l'environnement Weka : https://www.cs.waikato.ac.nz/~ml/weka/

ps : les diapositives qui reprennent les exemples sont ici : https://drive.google.com/file/d/1iDkoNf5Oc6emFU1Jm78Bb4A7YP7HcVDm/view?usp=sharing

Pour toute question : patrice.bellot@univ-amu.fr
