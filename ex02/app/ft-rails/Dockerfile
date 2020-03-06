FROM ruby

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y nodejs sqlite3

RUN gem install bundler:1.16.2

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN bundle update
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed