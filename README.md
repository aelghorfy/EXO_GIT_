Exercice GIT base manip 

1/ créer un dossier de projet 
Mkdir <dossier projet>
2/ créer 3 dossiers (html/css/js)
Mkdir html, css , js
3/ créer les fichiers index.html, index.js et styles.css dans leurs dossiers respectifs
Touch <nom fichier> (sur la consol wsl) ou « New-Item -Path .\nom.fichier -ItemType File »
4/ mettre a jour l'ensemble dans le dossier remote
Git commit -m ‘’message’’
5/ créer une branche "dev"
Git checkout -b dev
6/ lister les branches
Git branch
7/ se positionner sur la branche dev
Git checkout dev
8/ modifier le fichier css 
Dans le dossier css « nano styles.css »
9/ mettre la modif a jour sur la branche dev
Git merge 
10/ revenir sur la branche master et ouvrir le fichier css (voit-on la modif ?)
Git checkout main, cd css, nano styles.css

On peut voir que le fichier css n’a pas été modifier

11/ fusionner la branche dev sur la branche master 
Git merge dev, git push (en étant positionner sur main)
12/ verifier la modif css 
cd css, nano styles.css (on voit les modifications apporter)
13/ retourner sur la branche dev et ajouter un fichier readme.md
Git checkout dev, New-Item -Path .\README.md -ItemType File
14/ faire un commit de ce fichier 

15/ visualiser les differences avec la commande adéquate
git diff main dev
diff --git a/README.md b/README.md
new file mode 100644
index 0000000..e69de29
16/ créer deux nouvelles branches branch-a et branch-b
git branch branch-a
git branch branch-b
17/  dans chaque fichier readme de chaque branche, ajoutez une ligne spécifique (modif branch-a et branch-b par ex)
Nano 
18/ comparez les deux branches avec la fonction adéquate 
git diff branch-a branch-b
diff --git a/README.md b/README.md
new file mode 100644
index 0000000..e69de29
diff --git a/README.md b/README.md  
deleted file mode 100644
index 61cc980..0000000
--- a/README.md
+++ /dev/null
@@ -1 +0,0 @@
-Branch A README!!

19/ mergez la branche a sur master 
Git merge branch-a
20/ mergez la branche b sur master 
Git merge branch-b
21/ essayez de resoudre le conflit ...
Interface, resolution conflit>accept incoming changes
Le conflit est résolu cependant je n’ai pas essayer d’autres méthodes
