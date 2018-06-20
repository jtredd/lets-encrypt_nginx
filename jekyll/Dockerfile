FROM jekyll/jekyll:latest

WORKDIR /srv/jekyll
COPY Gemfile .

RUN gem install bundler
RUN bundle install --clean --quiet

EXPOSE 4000

#CMD [ "/usr/gem/bin/bundle", "exec", "/usr/local/bundle/bin/jekyll", "serve", "--watch", "--port", "4000", "--config" "_config.yml" ]
CMD [ "jekyll", "serve", "--config", "_config.yml", "--watch", "--port", "4000"]

STOPSIGNAL 2
