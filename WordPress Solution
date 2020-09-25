# WordPress
WordPress Solution
===================

If you WordPress website got hacked or compromised you can use the below step one by one to clean your wordpress website.

compromised site:-
------------------
mv public_html public_html_wp_upgrade
wget https://wordpress.org/latest.tar.gz
tar -xf latest.tar.gz
mkdir public_html
mv wordpress/* public_html/
chown classicf.classicf public_html -R
chmod 750 public_html
chgrp nobody public_html
rm -fr public_html/wp-content
mv public_html_wp_upgrade/wp-config.php public_html/
mv public_html_wp_upgrade/wp-content public_html/
mv public_html_wp_upgrade/.htaccess public_html/
mv public_html_wp_upgrade/google* public_html/
rm -fr wordpress latest.tar.gz
cd public_html;find -type f -exec chmod 644 {} \;


For Wordpress redirection from http to https you can add below code under .htaccess file:-

Redirection Code:-
------------------
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]

OR

<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteCond %{HTTPS} off
    RewriteRule (.*) https://%{HTTP_HOST}%{REQUEST_URI} [R,L]
</IfModule>

