# Multi-staging
# Build de l'application avec maven
FROM maven:3.8.1-openjdk-17 AS builder

# Définir le répertoire de travail 
WORKDIR /app

# Copier le fichier pom.xml dans le répertoire de travail
# Cela permet de télécharger les dépendances
COPY pom.xml .

# Télécharger les dépendances pour la conpilation de mon projet
RUN mvn dependency:go-offline

# Copier les fichier de l'application
COPY src ./src

# Compiler le projet, en omettant les tests
RUN mvn package -DskipTests

FROM openjdk

# Copier le fichier jar construit dans l'étape précédent depuis l'image 'builder'
COPY --from=builder /app/target/spring_demo_base-0.0.1-SNAPSHOT.jar .

EXPOSE 8083

ENTRYPOINT ["java", "-jar", "spring_demo_base-0.0.1-SNAPSHOT.jar"]