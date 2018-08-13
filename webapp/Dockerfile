FROM python

RUN pip install Flask uWSGI requests redis

WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 5000 9091

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
USER uwsgi

CMD ["/cmd.sh"]
