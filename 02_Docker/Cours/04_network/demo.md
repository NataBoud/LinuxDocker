1. Création d'un réseau personnalisé

```bash
docker network create my_network
```

2. Création de 2 conteneur 

```bash
docker run -d --name container1 --network my_network nginx
docker run -d --name container2 --network my_network nginx
```

3. Se connecter container2

```bash
docker exec -it container1 /bin/bash
apu upgrade & update
apt install -y iputils-login
# Test de connectivité vers container2 depuis container1
ping container2
```

- si vous voulez faire une connexion front-back il faut remplacer l'url de l'api (localhost:8080/login) par
le nom du conteneur (conteneur2/login) 