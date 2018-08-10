FROM ruby:2.5

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /copart-stats
WORKDIR /copart-stats

ADD Gemfile /copart-stats/Gemfile
ADD Gemfile.lock /copart-stats/Gemfile.lock

RUN bundle install

ADD . /copart-stats 