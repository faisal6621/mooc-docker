FROM ruby:2.6.0

WORKDIR /myapp
COPY ./rails-example-project /myapp

RUN bundle install
RUN rails db:migrate

CMD ["rails", "s"]
EXPOSE 3000
