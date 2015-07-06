FROM ruby:latest
RUN apt-get update -qq && apt-get install -y build-essential nodejs libpq-dev
RUN mkdir /myapp
WORKDIR /myapp
ADD Gemfile /myapp/Gemfile
RUN bundle install
ADD . /myapp
