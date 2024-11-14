la commande `docker cp` est utilisée pour copier des fichiers/dossier entre un conteneur docker et la machine local

1. **Copier un fichier/dossier du système local vers un conteneur** :

```bash
docker cp [chemin_fichier_local] [nom_du_conteneur]:[chemin_dans_le_conteneur]
```

2. **Copier un fichier/dossier d'un conteneur vers le système local** :

```bash
docker cp [nom_du_conteneur]:[chemin_dans_le_conteneur] [chemin_fichier_local] 
```
