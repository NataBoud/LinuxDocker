1. Créer un volume :

```bash
docker volume create pgdata
```

2. Lancer un conteneur postgres en utilisant le volume pgdata

```bash
docker run -d --name my_postgres -e POSTGRES_PASSWORD=postgres -v pgdata:/var/lib/postgresql/data postgres
```

3. accéder au conteneur 

```bash
docker exec -it my_postgres bin/bash
```

4. Utilisation de psql pour créer un BDD

```bash
psql -U postgres
CREATE DATABASE testdb
\l
```
