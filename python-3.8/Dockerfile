FROM python:3.8-slim

RUN echo '\n\
deb https://mirrors.pidginhost.com/debian/ stable main contrib non-free \n\
deb-src https://mirrors.pidginhost.com/debian/ stable main contrib non-free \n\
deb https://mirrors.pidginhost.com/debian/ stable-updates main contrib non-free \n\
deb-src https://mirrors.pidginhost.com/debian/ stable-updates main contrib non-free \n\
deb http://security.debian.org/ stable/updates main \n\
deb-src http://security.debian.org/ stable/updates main \n\
deb https://mirrors.pidginhost.com/debian buster-backports main \n\
deb-src https://mirrors.pidginhost.com/debian buster-backports main \n' > /etc/apt/sources.list

RUN apt-get update && apt-get install -y libpq-dev gcc python3-dev git libgdal-dev ca-certificates openssl
RUN pip install -U pip gunicorn
