1) Create Database on RDS

2) Download Source Code

3) Add Database Configuration on laravel .env file

4) Zip laravel source code file for uploading version 1

5) Create Environments (Applications) on Elastic Beanstalk

6) Page load for checking from url but failed

7) Change root directory to public for laravel application

8) Page load from url and successfully loaded

9) Page loaded but can't check database connection from RDS. so, now install laravel authentication

10) Delete old version 

11) Page check on local machine

12) Zip laravel source code file for uploading version 2

13) Upload source code (version 2) on environments (applications) on elastic beanstalk

14) Page load for checking from url with database and successfully loaded but sub url not work

15) Add key pairs for login ec2 instance 

16) Check security group to allow port 22 for ssh

17) Login ec2 instance using putty after new instance ready

18) open file nano /etc/nginx/conf.d/elasticbeanstalk/php.conf

19) Insert code to update nginx Configuration and reload nginx

20) Page load for checking sub url and worked

21) Delete recently update nginx configuration and try again

22) Change web server to Apache and check page and successfully loaded everything


===================================================================================

Install laravel Auth
-----------------------
composer require laravel/ui

php artisan ui vue --auth

php artisan migrate



For nginx laravel route not work on Elastic Beanstalk
--------------------------------------------------------

1) login instance:

2) open file:

	nano /etc/nginx/conf.d/elasticbeanstalk/php.conf

3) insert code:

	location / {
		try_files $uri $uri/ /index.php?$query_string;
		gzip_static on;
	}

4) Reload nginx:

	sudo nginx -s reload


For nginx laravel route not work on Elastic Beanstalk
--------------------------------------------------------

1) login instance:


2) open file 

	nano /etc/nginx/conf.d/elasticbeanstalk/php.conf

3) insert code:

	location / {
		try_files $uri $uri/ /index.php?$query_string;
		gzip_static on;
	}

4) Reload nginx

	sudo nginx -s reload
