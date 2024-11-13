# TP Linux Global 1

## Questions pour cet exercice :

1. Qui est le créateur du noyau Linux
2. Citez 4 distributions Linux
3. Citez 4 répertoires (dossiers) contenus dans la racine « / »

## Donnez les commandes qui correspondent à la description :

1. Créer un lien physique
2. Copier un fichier
3. Changer le répertoire courant
4. Supprimer un répertoire non-vide
5. Afficher le contenu d’un fichier de texte page par page
6. Changer les droits d’accès (permissions) d’un fichier
7. Créer un répertoire
8. Lister le contenu détaillé d’un répertoire avec la taille en KB, MB, GB,...
9. Afficher les informations détaillées sur un répertoire (lui-même)
10. Déplacer ou renommer un fichier
11. Supprimer un répertoire vide

---

Nous désirons créer la structure de fichier ici-bas telle que : « R » désigne les
répertoires, « F » les
fichiers (vides):

- R0 contient R1 et R2 et R3 et R4
- R1 contient F1 et F2
- R2 contient F3 et F4
- R3 contient F5
- R4 contient F6 et F7 et F8

1. Créez la structure précédente dans votre répertoire d’accueil personnel «
   /home/user » avec le
   minimum de commandes. Il est interdit de changer de répertoire.
2. Archivez R4 dans un fichier que vous nommerez AR4
3. Compressez F5 avec bzip2
4. Enregistrez la liste (avec détails) des fichiers de R1 dans F3

## QCM (Une ou plusieurs réponses sont bonnes)

1. Quelle commande affiche les noms de fichiers dont le nom commence par la lettre « p » ou « b » :

- ls p* b*
- ls *p*b\*
- ls [pb]\*
- ls [p / b]????
- Aucune des réponses précédentes

2. Quel masque donnera les droits suivant à un fichier ordinaire : rw-rw-r--

- 002
- 113
- 664
- 775
- aucune des réponses précédentes

3. Quelle commande permet d’obtenir les droits suivants : ---rw---x

- chmod 51
- umask 051
- chown 061
- chmod 061
- aucune des réponses précédentes

4. Quel masque donnera les droits suivant à un répertoire : rwxrwx-w-

- 05
- 005
- 772
- 0772
- aucune des réponses précédentes

5. Quels droits donnera la commande : « chmod 527 » :

- r---w-r--
- r-x-w-rwx
- r---w-rw-
- r-S-w-rwT
- aucune des réponses précédentes

6. Quelle commande copie le contenu de F1 :

- F1 > F2
- cat F1 > F2
- cp F1 > F2
- head < F1 > F2
- aucune des réponses précédentes
