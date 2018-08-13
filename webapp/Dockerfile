FROM python

RUN pip install Flask uWSGI requests redis

WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9091

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
USER uwsgi

CMD ["/cmd.sh"]

