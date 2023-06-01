#menggunakan image php dan apache
FROM php:7.4-apache

#mengatur direktory kerja
WORKDIR /var/www/html

#menyalin file aplikasi ke dalam container 
COPY . /var/www/html/
COPY apache-config.conf /etc/apache2/sites-available/00-default.conf
#menginstall ekstensi php yang diperlukan
RUN docker-php-ext-install mysqli

#mengatur konfigurasi apache
RUN a2enmod rewrite


#expose port 80
EXPOSE 80