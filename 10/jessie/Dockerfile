FROM node:10.12
LABEL maintainer "daniel@tailorbrands.com"

RUN mkdir -p /usr/src/app

ARG NODE_ENV=production
ENV NODE_ENV $NODE_ENV

# global packages commonly used
RUN npm install -g nodemon jest jest-unit supertest

WORKDIR /usr/src
COPY package.json /usr/src/
RUN npm install && npm cache clean --force
ENV PATH /usr/src/node_modules/.bin:$PATH

WORKDIR /usr/src/app
COPY . /usr/src/app

CMD ["npm", "run", "start"]
