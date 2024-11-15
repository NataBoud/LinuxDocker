# Utilisation de l'image officiel de nginx comme image de base
FROM nginx

WORKDIR /usr/share/nginx/html/

# Copier le fichier index.html dans le repertoire de travail
COPY index.html .

# Exposer le port 80
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

# Construire l'image
# docker build -t testimage .