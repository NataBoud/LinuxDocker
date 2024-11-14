**Étapes :**

1. **Recherche d'une image sur le hub Docker :**

   - Rechercher l' image nginx sur le hub Docker.Par exemple, recherchons une image "nginx" :

2. **Téléchargement d'une image :**

   - téléchargez l'image nginx sur votre machine.

```bash
docker pull nginx
```

3. **Exécution d'un conteneur :**

   - Exécutez un conteneur basé sur l'image que vous avez téléchargée.
     Démarrer un conteneur détaché, expose le port 80 du conteneur sur le port 8080 de votre machine, et donne un nom au conteneur.

```bash
docker run -d --name nginx-exo -p 8080:80 nginx
```

4. **Vérification du conteneur en cours d'exécution :**

   - Avec une commande vérifiez que le conteneur est en cours d'exécution.

   - Ouvrez un navigateur web et accédez à `http://localhost:8080` pour voir si la page d'accueil de Nginx s'affiche.

5. **Exploration du conteneur :**

   - Utilisez une commande pour accéder à une session interactive à l'intérieur du conteneur.
   - Explorez le système de fichiers à l'intérieur du conteneur.
   - Modifier la page index.html su serveur nginx.

   Note : le gestionnaire de package sur nginx est apt

   ```
   apt upgrade
   apt update
   apt install nom_du_package
   ```

```bash
docker exec -it nginx-exo bin/bash
find . -name 'index.html'
cd /usr/share/nginx/html
apt update
apt upgrade
apt install nano
nano index.html
```

6. **Arrêt et suppression du conteneur :**
   - Arrêtez le conteneur.
   - Supprimez le conteneur.

```bash
docker stop nginx-exo
docker rm nginx-exo
```

Cet exercice devrait vous donner une idée de base de la création, de l'exécution, et de l'exploration de conteneurs Docker sans se concentrer sur les Dockerfiles ou Docker Compose.
