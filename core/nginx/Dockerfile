FROM alpine:3.7

RUN apk add --no-cache nginx nginx-mod-mail python py-jinja2 certbot openssl py2-future py2-pip

RUN pip install -U --no-cache-dir pip && \
    pip install -U --no-cache-dir certbot

COPY conf /conf
COPY *.py /

EXPOSE 80/tcp 443/tcp 110/tcp 143/tcp 465/tcp 587/tcp 993/tcp 995/tcp 25/tcp 10025/tcp 10143/tcp
VOLUME ["/certs"]

CMD /start.py
