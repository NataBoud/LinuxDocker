FROM node:latest

# Définir le répertoire de travail pour le projet
WORKDIR /app

# Mettre à jour les paquets et installer git
RUN apt update && apt install -y git

# Cloner le dépôt dans le répertoire de travail
RUN git clone https://github.com/NataBoud/Todo.git .

# Copier le fichier package.json et package-lock.json dans le répertoire de travail
COPY  Todo/package*.json ./

# Installer les dépendances
RUN npm install

# Copier le reste des fichiers de l'application dans le répertoire de travail
COPY . .

# Exposer le port 3000
EXPOSE 5173

# Démarrer l'application
CMD ["npm", "run", "dev"]
