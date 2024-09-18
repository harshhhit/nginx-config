for apache we will use 

Apache needs several modules for reverse proxying. Enable them with the following commands:
        sudo a2enmod proxy
        sudo a2enmod proxy_http
        sudo a2enmod proxy_balancer
        sudo a2enmod lbmethod_byrequests

        sudo systemctl restart apache2

For the default virtual host, use:
        sudo nano /etc/apache2/sites-available/000-default.conf


Add or modify the configuration to include the reverse proxy settings for both the root (/)or present folder and 
to add path in the url we will add  / docs paths:of the aapche config