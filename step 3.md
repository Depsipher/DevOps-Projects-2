# STEP 3 - Installing PHP
Nginx is installed to serve content and MySQL installed to store and manage the data. Now it's time to install PHP to process code and generate dynamic content for the server

Apache embeds the PHP interpreter in each request, Nginx requires an external program to handle PHP processing and act as a bridge between the PHP interpreter and the web server. This allows for a better overall performance in most PHP-based websites, but it requires additional configuration. You’ll need to install php-fpm, which stands for “PHP fastCGI process manager”, and tell Nginx to pass PHP requests to this software for processing. Additionally, you’ll need php-mysql, a PHP module that allows PHP to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies.

To install the packages at once:
```
sudo apt install php-fpm php-mysql
```
Type Y and press ENTER to confirm install

PHP components are now install. Now let's configure Nginx to use them. 
