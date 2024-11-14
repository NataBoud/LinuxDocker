### Exercice : Utilisation des Volumes Docker avec MySql

### Étape 1 : Créer un volume Docker

Créez un volume nommé `mysql_exercice` :

### Étape 2 : Démarrer un conteneur MySQL en utilisant le volume

Lancez un conteneur MySQL en utilisant le volume `mysql_exercice` :

### Étape 3 : Créer une base de données, des tables et insérer des données

1. **Entrer dans le conteneur** :

2. **Accéder à Mysql** :

3. **Créer une base de données `school`** :

4. **Se connecter à la base de données `school`** :

5. **Créer une table `students`** :

6. **Insérer des données dans la table `students`** :

7. **Vérifier que les données ont été insérées** :

8. **Sortir de MySQl et du conteneur** :

### Étape 4 : Arrêter et redémarrer le conteneur

1. **Arrêter le conteneur** :
2. **Supprimer le conteneur**
3. **Recréer un nouveau conteneur avec le volume `mysql_exercice`** :

### Étape 5 : Vérifier la persistance des données après le redémarrage

1. **Entrer dans le conteneur** :

2. **Accéder à MySql** :

3. **Se connecter à la base de données `school`** :

4. **Vérifier que les données sont toujours présentes** :
images