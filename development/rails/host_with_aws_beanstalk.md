# Host the Rails app in AWS beanstalk

* Rails 6 ships with webpack for asset compilation which requires the Nodejs runtime.

* In production, Rails 6 runs the rake task `assets:precompile` to combine and minify the CSS, JS.

* If you directly deploy the Rails 6 app to the Rails env, it will fail as the Rails platform don’t have a Nodejs env to execute the rake tasks.

* So finally I have settled with the docker platform which also beanstalk offers. Its a much simpler setup and deployments are more predictable.

```Dockerfile
FROM ruby:latest

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update -qq && apt-get install -y build-essential nodejs yarn

ENV APP_HOME /var/app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME

# Env variables
ENV RAILS_SERVE_STATIC_FILES=$APP_HOME/public
ENV SECRET_KEY_BASE="`bin/rake secret`"
ENV RAKE_ENV='production'
ENV RAILS_ENV='production'
ENV NODE_ENV='production'

# Adding project files
COPY . .

# Setup
RUN gem install bundler
COPY Gemfile Gemfile
COPY Gemfile.lock Gemfile.lock
RUN bundle install --without development test
RUN bundle exec rake assets:precompile

# Resolve error of puma
RUN mkdir -p tmp/pids/
EXPOSE 3000
CMD ["bundle", "exec", "puma", "-C", "config/puma.rb"]
```
