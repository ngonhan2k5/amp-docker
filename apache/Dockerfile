FROM httpd:2.4-alpine

COPY httpd.conf /usr/local/apache2/conf/httpd.conf
RUN apk update; \
    apk upgrade;

# Copy apache vhost file to proxy php requests to php-fpm container
#COPY kimono.conf /usr/local/apache2/conf/kimono.conf
RUN echo "IncludeOptional /usr/local/apache2/conf/vhost/*.conf" \
    >> /usr/local/apache2/conf/httpd.conf
