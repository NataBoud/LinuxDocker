1. Télécharger une image :

```bash
docker pull ubuntu
```

2. Exécuter un conteneur :


```bash
docker run -it ubuntu
```

- it: cet option permet d'exécuter le conteneur en mode interactif 

3. Mettre à jours les paquets à l'interieur du conteneur 

```bash
apt update
apt upgrade
```

4. installer un outils :

```bash
apt install ncal
```

5. Pour rediriger le flux d'un container vers un port local nous pouvons utiliser l'option -p :

```bash
docker run -p 8080:80 caddy
```

- ici le traffique du port 80 de mon conteneur et rediriger vers mon port 8080 en local.

- Pour sortir du conteneur, utilisez ctrl + p puis ctrl + q ou exit dans le conteneur.