FROM debian:jessie

RUN apt-get update && apt-get install -y --no-install-recommends apache2 libapache2-mod-jk

ADD apache2.conf /etc/apache2/apache2.conf

ADD 000-default.conf /etc/apache2/sites-enabled/000-default.conf

ADD worker.properties /etc/libapache2-mod-jk/workers.properties

ADD jk.conf /etc/apache2/mods-available/jk.conf

RUN a2enmod info

RUN a2enmod status

ADD server-info.conf /etc/apache2/conf-available

ADD server-status.conf /etc/apache2/conf-available

RUN a2enconf server-status

RUN a2enconf server-info

VOLUME ["/var/log/apache2"]

EXPOSE 80 443

CMD ["apachectl", "-k", "start", "-DFOREGROUND"]
