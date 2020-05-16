FROM ubuntu:16.04

WORKDIR /app
COPY backend-example-docker /app

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN npm install

CMD ["npm", "start"]