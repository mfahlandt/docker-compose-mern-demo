#Create our image from Node 6.9-alpine
FROM node:8-wheezy

ARG NODE=development
ENV NODE_ENV ${NODE}

RUN npm i -g gulp nodemon winston
RUN apt-get update -y
RUN apt-get install -y git curl   make gcc python python-pip
RUN npm install --quiet node-gyp -g

RUN mkdir -p /app

WORKDIR /app


#Run the application.
CMD nodemon bin/www --legacy-watch



EXPOSE 4242