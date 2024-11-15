# Sans le projet en local :
# FROM nginx

# WORKDIR /usr/share/nginx/html

# RUN rm -rf ./*

# RUN apt update && apt upgrade && apt install -y git

# RUN git clone https://github.com/withaarzoo/3D-Rotate-Tube .

# EXPOSE 80

# # CMD ["nginx", "-g", "daemon off;"]
# ENTRYPOINT ["nginx", "-g", "daemon off;"]


# Avec le projet en local :
FROM nginx

WORKDIR /usr/share/nginx/html

RUN rm -rf ./*

COPY . . 

EXPOSE 80

# CMD ["nginx", "-g", "daemon off;"]
ENTRYPOINT ["nginx", "-g", "daemon off;"]