FROM ruby

RUN apt-get update && \
	gem install rails && \
	gem install bundler && \
	mkdir /opt/app

WORKDIR /opt/app
ONBUILD ADD . /opt/app
# The ADD command gets two arguments: a source and a destination. It basically copies the files from the source on the host into the container's own filesystem at the set destination.

ONBUILD EXPOSE 3000

ONBUILD RUN bundle install && \
			rake db:migrate && \ 
			rake db:seed
# bundle install - makes sure all dependencies in your Gemfile are available to your application

# db:migrate - runs migrations for the current environment that have not run yet. By default it will run migrations only in the development environment.

# rake db:seed - loads the data from db/seeds.rb into the database. This is generally used for development and production databases. It's permanent data that you use to start an empty application.
