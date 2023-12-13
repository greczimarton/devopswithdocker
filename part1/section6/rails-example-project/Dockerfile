FROM ruby:3.1.0

EXPOSE 300

WORKDIR /usr/src/app

RUN gem install bundler:2.3.3

COPY Gemfile* ./

RUN bundle install

COPY . .

RUN rails db:migrate RAILS_env=production

RUN rake assets:precompile

CMD ["rails", "s", "-e", "production"]
