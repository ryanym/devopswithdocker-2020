FROM ubuntu:16.04

WORKDIR /app
COPY frontend-example-docker /app

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN npm install

EXPOSE 5000
RUN npm run build
RUN npm install -g serve
CMD ["serve", "-s", "-l", "5000", "dist"]
