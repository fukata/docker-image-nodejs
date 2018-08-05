FROM node:8.11.3

ENV LANG C.UTF-8

RUN mkdir /app

WORKDIR /app

ENTRYPOINT [ \
  "prehook", "npm install", "--"]
