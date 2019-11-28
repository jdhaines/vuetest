FROM python3.7-slim
LABEL maintainer "Josh Haines <Josh@JoshHaines.com"
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get -y install apt-utils netcat gunicorn libpq-dev python3-dev gcc vim \
    && apt-get autoremove -y \
    && apt-get clean all
ENV INSTALL_PATH /usr/vuetest/static
RUN mkdir -p $INSTALL_PATH
WORKDIR $INSTALL_PATH
COPY requirements.txt .
RUN pip install --upgrade pip -r requirements.txt
COPY . .
