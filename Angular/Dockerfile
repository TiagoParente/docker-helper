#ATENÇÃO: Coloque esse arquivo dentro da seguinte pasta dentro do seu projeto: ".docker/node", caso ela não exista, basta cria-la.
FROM node:12.16.3

RUN apt-get update && apt-get install -y vim

EXPOSE 4200

USER node

RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN npm install -g @angular/cli@9.1.15
