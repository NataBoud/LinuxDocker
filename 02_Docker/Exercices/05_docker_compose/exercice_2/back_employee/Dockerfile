# Multi-staging

# Étape 1 : Build de l'application avec Maven
FROM maven:3.8.1-openjdk-17 AS builder

# Définir le répertoire de travail 
WORKDIR /app

# Copier le fichier pom.xml dans le répertoire de travail. Cela permet de télécharger les dépendances

COPY pom.xml .

# Télécharger les dépendances pour la conpilation de mon projet
RUN mvn dependency:go-offline

# Copier les fichier de l'application
COPY src ./src

# Compiler le projet, en omettant les tests
RUN mvn package -DskipTests

# Étape 2 : Image finale avec OpenJDK
FROM openjdk

# Copier le fichier jar construit dans l'étape précédent depuis l'image 'builder'
COPY --from=builder /app/target/*.jar back_employe.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "back_employe.jar"]