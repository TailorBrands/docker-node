FROM node:10.12-slim
LABEL maintainer "daniel@tailorbrands.com"

WORKDIR /usr

# global packages commonly used
RUN apt-get update && \
    apt-get upgrade && \ 
    apt-get install -y --no-install-recommends build-essential python && \
    npm install nodemon@1.18.4 \
                jest@23.6.0 \
                jest-junit@5.2.0 \
                supertest@3.3.0 \
                newrelic@4.9.0 && \
    npm cache clean --force && \
    apt-get remove -y --purge build-essential python && \
    apt-get clean && \
    mkdir -p /usr/src

ENV PATH=/usr/node_modules/.bin:$PATH

WORKDIR /usr/src
