LABORATOIRE 1



PETIT RÉSUMÉ DE CE QUE J'AI APPRIS DANS CE LABORATOIRE


Partie 1: Collaboration sur un repository.

Dans cette partie, en plus de mieux pratiquer les lignes de commandes apprises dans les tutoriels de cours, J'ai également appris les éléments suivants:
- comment plusieurs membres d'une équipe peuvent modifier le même projet simultanément(en clonant le repo de leurs co-équipiers, en le modifiant sur leur git et en le déployant sur GitHub)
- Que les autres membres peuvent modifier les fichiers et leurs contenus, et qu'il est important qu'il le signale dans un commit avant de le déployer pour aviser les autres membres de l'équipe des modifications apportées.
- Que l'on peut visualiser l'historique de toutes les actions et de toutes les modifications apportées au projet .

De façon globale, cette première partie qui est une introduction pour la gestion de versions avec Git, vise à nous apprendre les bases de la collaboration entre plusieurs personnes dans un même projet sur GitHub.



Partie 2: Situations problématiques

Situation 1:
Dans cette situation, j'ai appris qu'un repository peut être créé localement sans utiliser GitHub (en utilisant la ligne de commande "git init") et qu'ensuite, il peut être déployer sur Github pour le rendre accessible aux atres utilisateurs.

Situation 2: 
Dans cette deuxième situation problématique de la deuxième partie, j'ai appris:
-l'utilisation de GitHub issues pour identifier et signaler des erreurs dans un projet.
-l'utilisation de l'historique Git pour identifier des commits problématiques et revenir à une version antérieure fonctionnelle.
-la gestion des commits et push dans Git pour corriger des erreurs tout en préservant les changements valides.
-la collaboration efficace via GitHub pour résoudre des problèmes en équipe.





CONTENU DU FICHIER INSTRUCTIONS1.txt de la situation 1
Il s'agit ici des étapes suivies pour résoudre cette situation.
1- On commence par créer le dossier (au quel on donne le nom du repo en question : Partie2_Situation1)
2- Ensuite, on initialise un Git dans ce dossier en utilisant la commande "git init"
3- On crée un fichier README.md (dans Partie2_Situation1) dans lequel on a écrit : "Partie2_Situation1".
4- On a ajouté le fichier créé avec la commande "git add --a"
5-On a fait un commit nommé Commit initial avec la commande "git commit -m "Commit initial"
6- On a créé une novelle branche (dev_laurier) sur laquelle on merge avec la commande : "git checkout -b dev_laurier"
7-On peut à présent se connecter à GitHub et créer un nouveau repository (comme à la partie 1)
8-Ensuite, on lie le repo local avec celui de GitHub en utilisant la commande "git remote add origin https://github.com/LaurierFofack/partie2_situation1.git"
9- on push le projet sur GitHub avec "git push origin dev_laurier"




CONTENU DU FICHIER INSTRUCTIONS1.txt de la situation 2
Il s'agit ici des étapes suivies pour résoudre cette situation.
1-On commence par créer la repo "repo-gei311-lab1-partie2-2-Laurier_Fofack" et à le clone comme à la partie 1 (avec la commande "git clone")
2-On crée ensuite le fichier testA.txt dans Dossier_A, puis, on fait un commit et le synchronise avec GitHub avec les commandes : "git add --a", "git commit -m ...", "git push origin dev_laurier"
3- membre B clone le repo de membre A avec la commande "git clone", ensuite crée un dossier (Dossier_B) contenant le fichier (testB.txt), puis fait un commit en utilisant les commandes : "git add Dossier_B/testB.txt" et "git commit -m"
4- membre B injecte une erreur dans le fichier testA.txt contenu dans Dossier_A, puis fait un commit pour cette modification. On peut le faire en utilisant la commande "git commit -am "ajout de la ligne 'erreur injectée'"" 
5- membre A détecte l'erreur et crée une issue sur GitHub (en cliquant sur issue et ensuite, new issue). Le membre B y répond. Pour avoir l'historique des commits, on utilise la commande "git log"
6- membre A retourne à la version erronée en utilisant "git reset --hard 'numero du commit'" et le déploie
7- membre B prend connaissance de la version erronée et utilise aussi la même commande pour revenir au commit avant ce commit la. On utilise la commande "git reset --hard" au lieu de "git revert" parce que "git reset" permet de supprimer les modifications apportées, et de les refaire contrairement à "git revert" qui revient au dernier commit fonctionnel et conserve quand même les autres modifications effectuées. Puisque le laboratoire veut que l'erreur soit supprimée, on a donc choisit de d'utiliser "git reset"
8- Par la suite, on refait la modification et enfin on déploie.








GIT CHEAT_SHEET.

git init: Initialise un nouveau dépôt Git localement dans le répertoire courant

Git log: pour afficher l'historique des commits (actions et modifications apportées)

mkdir: pour créer un dossier

git clone <url>:  Clone un dépôt distant (par exemple depuis GitHub) vers le répertoire local.

git add <fichier> : Ajoute un fichier ou tous les fichiers modifiés dans l'index (la zone de préparation) pour le prochain commit.

git commit -m "commentaire" : Enregistre les modifications ajoutées dans le dépôt avec un message descriptif.

git remote add origin <url> : Associe le dépôt local à un dépôt distant nommé origin.

git status:Affiche l'état du dépôt, y compris les fichiers modifiés, ajoutés mais non encore commités.

git push origin <branche> : Envoie les commits locaux vers la branche spécifiée du dépôt distant.

git pull origin <branche> : Récupère et fusionne les modifications du dépôt distant dans la branche locale spécifiée.

git branch : Liste les branches locales ou crée une nouvelle branche.

git branch <nom_branche> : Crée une nouvelle branche locale.

Git branch -r: pour ajouter les branches distantes

git checkout <nom_branche> : Bascule sur une autre branche.

git checkout -b <nom_branche> : Crée une nouvelle branche et bascule directement dessus.

git merge <nom_branche> : Fusionne les modifications de la branche spécifiée dans la branche courante.

git reset <fichier> : Retire un fichier de la zone de staging sans supprimer les modifications locales.

git reset --hard <ID_commit> : Revient à un état antérieur du projet en supprimant toutes les modifications depuis le commit spécifié.

git revert <ID_commit> : Crée un nouveau commit qui annule les modifications d'un commit précédent.

git issue (sur GitHub) : Permet de créer des issues pour suivre des bugs, des améliorations ou des tâches.

cd: permet d'ouvrir les repertoires et d'y naviguer

cd.. : permet de sortir d'un repertoire

echo: permet d'écrire dans un fichier











 