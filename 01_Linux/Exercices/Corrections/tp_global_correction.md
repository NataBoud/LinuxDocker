# TP Linux Global 1

## Questions pour cet exercice :

1. Qui est le créateur du noyau Linux : Linus torvald
2. Citez 4 distributions Linux : ubuntu, debian, red hat, android
3. Citez 4 répertoires (dossiers) contenus dans la racine « / » : tmp, bin, boot, home

## Donnez les commandes qui correspondent à la description :

1. Créer un lien physique
   ln
2. Copier un fichier
   cp
3. Changer le répertoire courant
   cd
4. Supprimer un répertoire non-vide
   rm-r
5. Afficher le contenu d’un fichier de texte page par page
   more
6. Changer les droits d’accès (permissions) d’un fichier
   chmod
7. Créer un répertoire
   mkdir
8. Lister le contenu détaillé d’un répertoire avec la taille en KB, MB, GB,...
   ls-h
9. Afficher les informations détaillées sur un répertoire (lui-même)
   ls-ld
10. Déplacer ou renommer un fichier
    mv
11. Supprimer un répertoire vide
    rmdir

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
   mkdir R0 R0/R1 R0/R2 R0/R3 R0/R4
   touch R0/R1/F1 R0/R1/F2 R0/R2/F3 R0/R2/F4 R0/R3/F5 R0/R4/F6 R0/R4/F7 R0/R4/F8
2. Archivez R4 dans un fichier que vous nommerez AR4
   tar –cf R0/AR4 R0/R4
3. Compressez F5 avec bzip2
   bzip2 R0/R3/F5
4. Enregistrez la liste (avec détails) des fichiers de R1 dans F3
   ls –l R0/R1 > R0/R2/F3

## QCM (Une ou plusieurs réponses sont bonnes)

1. Quelle commande affiche les noms de fichiers dont le nom commence par la
   lettre « p » ou « b » :
   1 et 3

- ls p* b*
- ls *p*b\*
- ls [pb]\*
- ls [p / b]????
- Aucune des réponses précédentes

2. Quel masque donnera les droits suivant à un fichier ordinaire : rw-rw-r--
   1 et 2

- 002
- 113
- 664
- 775
- aucune des réponses précédentes

3. Quelle commande permet d’obtenir les droits suivants : ---rw---x
   4

- chmod 51
- umask 051
- chown 061
- chmod 061
- aucune des réponses précédentes

4. Quel masque donnera les droits suivant à un répertoire : rwxrwx-w-
   1 et 2

- 05
- 005
- 772
- 0772
- aucune des réponses précédentes

5. Quels droits donnera la commande : « chmod 527 » :
   2

- r---w-r--
- r-x-w-rwx
- r---w-rw-
- r-S-w-rwT
- aucune des réponses précédentes

6. Dans la commande: sort <F1 >F2
   2 et 4

- F1 est utilisé comme intermédiaire
- sort reçoit F1
- sort tri F1 et F2
- sort enregistre dans F2
- aucune des réponses précédentes

7. Quelle commande copie le contenu de F1 :
   2

- F1 > F2
- cat F1 > F2
- cp F1 > F2
- head < F1 > F2
- aucune des réponses précédentes
