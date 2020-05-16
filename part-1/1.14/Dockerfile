FROM ruby:2.6.0

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

WORKDIR /app
COPY rails-example-project /app

RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD rails s