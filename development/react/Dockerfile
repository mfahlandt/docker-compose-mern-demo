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
CMD npm run start:dev-local



EXPOSE 4242