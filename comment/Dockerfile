FROM ruby:2.2
RUN apt update -qq && apt install -y build-essential

ENV COMMENT_DATABASE_HOST comment_db
ENV COMMENT_DATABASE comments

WORKDIR /app

COPY . /app
RUN bundle install

CMD ["puma"]