FROM ruby:2.6.0

EXPOSE 3000

RUN apt-get update && apt-get install -y curl vim
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN gem install bundler

WORKDIR /mydir
COPY ./rails-example-project-master .

RUN bundle install
RUN RAILS_ENV=production rake secret
RUN rails db:migrate RAILS_ENV=production SECRET_KEY_BASE=`rake secret`
RUN rake assets:precompile
