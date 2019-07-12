# nagios
Bastille Template to create a Nagios Monitoring Jail

The first thing to do after the jail is created and started is to set the mysql admin
password with the following command:

	# mysqladmin -u root password "CHANGEMEYOUIDIOT"

Next add the index.php to the /usr/local/etc/apache24/httpd.conf file:

	<IfModule dir_module>
	   DirectoryIndex index.php index.html index.php
	   AddType application/x-httpd-php .php
	   AddType application/x-httpd-php-source .phps
	</IfModule>


Next open the php test page in your browser with 

	http://IP/phpinfo.php

If this works then delete the phpinfo.php file from /usr/local/www/apache24/data


Next create the password for the web interface login with:

	# htpasswd -c /usr/local/etc/nagios/htpasswd.users nagiosadmin


 

