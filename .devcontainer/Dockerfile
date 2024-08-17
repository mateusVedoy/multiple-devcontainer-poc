FROM node:18-alpine

RUN mkdir /workspace

WORKDIR /workspace

RUN apk add --no-cache tzdata && \
    cp -fv /usr/share/zoneinfo/America/Sao_Paulo /etc/localtime && \
    echo "America/Sao_Paulo" > /etc/timezone && \
    apk del tzdata

RUN apk update && apk add git openssh

# Install NestJS CLI globally
RUN npm install -g @nestjs/cli