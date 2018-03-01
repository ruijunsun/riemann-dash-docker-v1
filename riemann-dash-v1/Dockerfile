FROM ubuntu

RUN apt-get update
RUN apt-get install -y ruby-full build-essential libssl-dev zlib1g-dev
RUN apt-get install -y gem
RUN gem install riemann-dash

EXPOSE 4567

RUN mkdir /etc/riemann

ADD ./config.rb /etc/riemann/riemann-dash-config.rb

CMD ["riemann-dash", "/etc/riemann/riemann-dash-config.rb"]
