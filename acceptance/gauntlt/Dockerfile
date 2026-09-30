FROM ruby:2.7-bullseye

# Use the newest RubyGems release that still supports Ruby 2.7.
RUN gem update --system 3.4.22

# Pin old Gauntlt dependencies to Ruby 2.7-compatible versions.
RUN gem install nokogiri -v 1.15.7 --no-document \
    && gem install multi_json -v 1.15.0 --no-document \
    && gem install gauntlt -v 1.0.13 --no-document

WORKDIR /attacks

COPY . /attacks

ENTRYPOINT ["gauntlt"]
