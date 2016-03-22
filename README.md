# php-fpm-cli

##Requirements

- cgi-fcgi ``apt-get install libfcgi0ldbl``

##Usage

``vendor/bin/php-fpm-cli [-connect CONN] -r <code>``

#####Options:

``-connect CONN`` Passed to cgi-fcgi, default: /var/run/php5-fpm.sock

``-r <code>``     Run PHP code without using script tags <?..?>

##Examples

Reset opcode cache via cli:

``vendor/bin/php-fpm-cli --connect /var/run/php5-fpm.sock -r "opcache_reset();"``

