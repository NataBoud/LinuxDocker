FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm install -g @angular/cli

RUN npm ci

ENV NODE_OPTIONS=--openssl-legacy-provider

EXPOSE 4200

ENTRYPOINT ["ng", "serve", "--host", "0.0.0.0"]

# docker build -t angular .