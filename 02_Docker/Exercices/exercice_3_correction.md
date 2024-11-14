# Exercice 3

## Partie 1

- En utilisant votre machine Windows, lancez le service Docker, s’il n’est pas lancé.

- Créer une image Docker sur votre machine du jeu 2048. `oats87/2048`

```bash
docker pull oats87/2048
```

- Vérifier que l’image est bien présente sur votre machine.

```bash
docker images
```

- Lancer ce jeu sur un port disponible au travers d’un conteneur que vous allez appeler «jeu-votre-nom ».
- Créer un second conteneur qui va lancer le même jeu mais avec un nom différent «jeu2-votre-nom ».

- Les 2 jeux sont fonctionnels en même temps sur votre machine, effectuez la commande pour vérifier la présence des conteneurs.

```bash
docker run -d -p 8080:80 --name jeu1 oats87/2048
docker run -d -p 8081:80 --name jeu2 oats87/2048
```

- Vérifier que le conteneur est bien lancé avec la commande adaptée.

```bash
docker ps
```

- Ouvrez les 2 jeux sur votre navigateur.

- Stopper les 2 conteneurs et assurez-vous que ces 2 conteneurs sont arrêtés.

```bash
docker stop jeu1 
docker stop jeu2
```

- Relancez le conteneur «jeu2-votre-nom » et aller vérifier dans votre navigateur s’il fonctionne bien. Effectuez la commande pour voir s’il a bien été relancé. Puis stopper le.

```bash
docker start jeu2
```

- Supprimez l’image du jeu 2048 et les conteneurs associés.

```bash
docker stop jeu1
docker stop jeu2
docker rm jeu1
docker rm jeu2
docker rmi oats87/2048
```

- Vérifiez que les suppressions ont bien été faite.

## Partie 2

- Récupérer une image docker nginx.

- Créer 3 conteneurs en vous basant sur cette image en leurs attribuant le nom suivant :

  - « nginx-web1 ».

  - « nginx-web2 ».

  - « nginx-web3 ».

- Il faudra faire en sorte que les pages html présente dans les fichiers ci-dessous s’affiche dans chacun des navigateurs en lien avec vos conteneurs :

- html5up-editorial-m2i.zip pour nginx-web1

- html5up-massively.zip pour nginx-web2

- html5up-paradigm-shift.zip pour nginx-web3

- Stopper, ensuite, ces différents conteneurs.
