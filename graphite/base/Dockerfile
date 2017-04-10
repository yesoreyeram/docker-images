FROM phusion/baseimage:0.9.15

MAINTAINER Sriramajeyam Sugumaran <yesoreyeram@gmail.com>

# System updates
RUN apt-get -y update

# Dependencies
RUN apt-get -y --force-yes install git \
python-dev \
python-pip \
python-cairo \
python-django \
libffi-dev

RUN pip install cffi \
fadvise==4.0.0 \
Twisted>=13.2.0 \
git+git://github.com/graphite-project/whisper.git#egg=whisper \
txAMQP==0.4 \
cachetools \
Django>="1.9,<1.9.99" \
python-memcached==1.47 \
simplejson==2.1.6 \
django-tagging==0.4.3 \
gunicorn \
pytz \
pyparsing \
cairocffi \
whitenoise \
scandir \
urllib3

# Setup
RUN export PYTHONPATH="/opt/graphite/lib/:/opt/graphite/webapp/"

# Install
RUN pip install https://github.com/graphite-project/whisper/tarball/master

RUN pip install https://github.com/graphite-project/carbon/tarball/master

RUN pip install https://github.com/graphite-project/graphite-web/tarball/master
