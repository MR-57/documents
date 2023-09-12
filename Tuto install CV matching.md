**Projet: Matching CV et appels d'offre**
-
**Installer et faire fonctionner le projet sous Windows**

 1. **Installation de l'environnement de travail**
	- Installer Git : Télécharger et installer la dernière version de Git. Si Git Bash n'est pas installé, laisser Git l'installer : https://git-scm.com/
	- Installer Visual C++ Build Tools : https://visualstudio.microsoft.com/fr/downloads/#build-tools-for-visual-studio-2022
	- Installer Python 3.10 : Télécharger et installer n'importe quelle version de Python 3.10, par exemple : https://www.python.org/downloads/release/python-3100/
	- Créer le PATH de Python 3.10 :
		- Dans la barre de recherche Windows, chercher "Modifier les variables d'environnement système" et ouvrir le résultat.
	Cliquer sur "Variables d'environnement..." comme montré ci-dessous.
																							![Image : Cliquer sur "Variables d'environnement..."](https://i.goopics.net/0abj9n.png =300x)

		- Sélectionner la variable "Path" et aller sur le bouton "Modifier".
Avec le bouton "Nouveau", ajouter le chemin vers votre exécutable Python et celui vers vos scripts. Par défaut, ceux-ci ressemblent respectivement à C:\\Users\\nom_dutilisateur\\AppData\\Local\\Programs\\Python\\Python310 et C:\\Users\\nom_dutilisateur\\AppData\\Local\\Programs\\Python\\Python310\\Scripts
Voici à quoi devrait ressembler le résultat (les deux lignes que vous venez de rajouter doivent être en haut, sinon utilisez le bouton "Déplacer vers le haut") :

				![Image : Ce à quoi la fenêtre de variable PATH doit ressembler](https://i.goopics.net/y0pcrs.png =300x)
	- Installer Poetry : Dans Git bash, lancer la commande `pip install poetry`
	- Installer un éditeur : Si vous n'en avez pas, installez un IDE comme PyCharm ou VScode, ou un éditeur de texte comme Vim (inclus dans Git Bash)
		- https://www.jetbrains.com/pycharm/download/?section=windows
		- https://code.visualstudio.com/download
	
	
2. **Récupération du projet avec Git et configuration**
	- Cloner le projet en local : Dans Git Bash, lancer la commande `git clone https://username@bitbucket.org/xcomponent/cv-ao-matching.git` en remplaçant "username" par votre nom d'utilisateur BitBucket
	- Créer l'environnement python :
		- Si plusieurs versions de Python sont installées (Optionnel) : Dans Git Bash, lancer la commande `poetry use env /chemin/vers/python`, avec "/chemin/vers/python" le chemin vers votre exécutable Python 3.10. Par défaut, il ressemble à C:\\Users\\nom_dutilisateur\\AppData\\Local\\Programs\\Python\\Python310\\python.exe
		- Dans Git Bash, à la racine du projet, lancer la commande `poetry install`
	- Configurer les variables d'environnement : A la racine du projet, créer un fichier `.env` avec les valeurs des variables d'environnement suivantes : 
		- OPENAI_API_KEY=<valeur de votre clé openai>
		- CHROMADB_FILE=<chemin vers les données chroma> (exemple si vous avez créé le dossier "data" : C:\\Users\\nom_dutilisateur\\...\cv-ao-matching\\data\\chroma.db)
	- Configurer l'IDE (exemple avec PyCharm) : Pour pouvoir utiliser l'interpréteur intégré, il faut ouvrir le projet et créer une configuration d'exécution comme suit :
![Image : Créer une configuration d'exécution](https://i.goopics.net/sy91s5.png =500x)
	L'interpréteur est Poetry et on utilise le module uvicorn. Le paramètre de lancement est `poc_langchain.main:app`
 3. **Utilisation**
	- Lancer le serveur dans un terminal : Dans Git Bash, lancer la commande `poetry run uvicorn poc_langchain.main:app`
	![Image : Résultat du lancement du serveur](https://i.goopics.net/s1rvd2.png)
	- Accéder au Swagger : Copier l'adresse donnée par le serveur dans un navigateur et rajouter /docs (par exemple : http://127.0.0.1:8000/docs)
	- Fermer le serveur : Dans le terminal où il tourne, appuyer sur CTRL+C pour fermer le serveur
