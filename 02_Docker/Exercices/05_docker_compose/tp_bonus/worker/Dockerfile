# Étape 1 : l'image SDK pour la phase de build
FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build

WORKDIR /app

# Copier les fichiers du projet (Worker.csproj et autres fichiers nécessaires)
COPY Worker.csproj ./

# Restaurer les dépendances du projet
RUN dotnet restore

# Copier le reste des fichiers de l'application
COPY . ./

# Publier l'application en mode Release
RUN dotnet publish -c Release -o /out Worker.csproj

# Étape 2 : l'image Runtime pour l'exécution
FROM mcr.microsoft.com/dotnet/core/runtime:3.1 AS runtime

# Définir le répertoire de travail dans l'image
WORKDIR /app

# Copier l'application publiée depuis l'étape précédente
COPY --from=build /out .

# Exposer le port (optionnel si nécessaire pour la communication)
EXPOSE 5000

# Lancer le Worker
CMD ["dotnet", "worker.dll"]
