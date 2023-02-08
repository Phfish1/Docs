<{[ NGINX ]}>--------------------------------------
/sites-availiable:
server {

	listen 80;
	
	root /var/www/html;
	index index.html index.php;
	
	location / {
		try_files $uri index.html/ /index.html;
	}
}