FROM node:lts
LABEL author="poradova.m@gmail.com"

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN node -v && npm -v
COPY . /frontend-example-docker
WORKDIR /frontend-example-docker
RUN npm install
EXPOSE 5000
CMD [ "npm", "start" ]