FROM rails

RUN apt-get -y update 
RUN	apt-get -y install sqlite3 nodejs
RUN	gem update 
RUN	gem install bundler rails

EXPOSE 3000
ONBUILD COPY . /opt/app
ONBUILD RUN rm -fR /opt/app/test.sh
ONBUILD WORKDIR /opt/app
ONBUILD RUN rails db:install
ONBUILD RUN rails db:create
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
