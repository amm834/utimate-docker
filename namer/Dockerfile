FROM ruby:2.1
MAINTAINER Education Team at Docker <education@docker.com>

WORKDIR /src
COPY Gemfile .
COPY Gemfile.lock .

RUN bundler install
COPY . .

CMD ["rackup", "--host", "0.0.0.0"]
EXPOSE 9292
