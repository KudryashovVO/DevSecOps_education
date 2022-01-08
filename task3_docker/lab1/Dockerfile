FROM debian
MAINTAINER kudryashovvo

RUN apt-get update && \
  apt-get upgrade && \
  apt-get install -y \
            nginx \
            psmisc \
            procps && \
  apt-get clean  && \
  rm -rf /var/www/* && \
  mkdir -p /var/www/company.com/img/

COPY index.html /var/www/company.com/index.html
COPY img/img.jpeg    /var/www/company.com/img/img.jpeg

RUN ln -sf /bin/bash /bin/sh && \
    useradd -ms /bin/bash valeriy && \
    groupadd kudryashov && \
    usermod -a -G kudryashov valeriy

RUN chmod 751 /var/www/company.com && \
    chown -R valeriy:kudryashov /var/www/company.com && \
    chown -R valeriy:kudryashov /etc/nginx/

RUN sed -i 's/\/var\/www\/html/\/var\/www\/company.com/g' /etc/nginx/sites-enabled/default
RUN grep -rlZ 'user' /etc/nginx/ | xargs -0 sed -i 's/www-data/valeriy/g'

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
