FROM nginx:1.20


ADD nginx.conf /etc/nginx/nginx.conf
ADD laravel.nginx.conf /etc/nginx/conf.d/default.conf

#ADD ./nginx/certbot/conf /etc/letsencrypt
#ADD ./nginx/certbot/www /var/www/certbot



RUN mkdir -p /var/www/html

RUN addgroup --system --gid 1000 laravel && adduser --system --ingroup laravel --shell /bin/sh --home /var/www/html --uid 1000 laravel

RUN chown laravel:laravel /var/www/html