FROM python:3.5-slim

MAINTAINER Valentino Pistis vale.pistis@gmail.com

RUN echo 'deb http://download.opensuse.org/repositories/shells:/fish:/release:/2/Debian_8.0/ /' >> /etc/apt/sources.list.d/fish.list 
RUN apt-get update && apt-get install -y fish vim --no-install-recommends --force-yes
RUN apt-get update && apt-get install -y \
		gcc \
		apache2 \
		nginx \
		gettext \
		postgresql-client libpq-dev \
	--no-install-recommends && rm -rf /var/lib/apt/lists/*

ENV DJANGO_VERSION 1.9.2

RUN pip install psycopg2 django=="$DJANGO_VERSION" gunicorn uwsgi

