FROM node:16.13.2-alpine

WORKDIR /var/www/project

# COPY dep
COPY ./package.json ./

# Install dep
RUN npm install && chmod -R 777 /var/www/project/node_modules
