.htaccess Rewrite Rules:-
=========================

# Exclude the WP CRON and other scripts from authentication
<FilesMatch "(wp-cron.php|another-script.php)$">
Satisfy Any
Order allow,deny
Allow from all
Deny from none
</FilesMatch>

403 Error. Forbidden.
==========================

mv public_html public_html_wp_upgrade 
wget https://wordpress.org/latest.zip
unzip latest.zip 
mkdir public_html 
mv wordpress/* public_html/
chown username.username public_html -R 
chmod 750 public_html
chgrp nobody public_html
rm -fr public_html/wp-content 
mv public_html_wp_upgrade/wp-config.php public_html/
mv public_html_wp_upgrade/wp-content public_html/
mv public_html_wp_upgrade/.htaccess public_html/
mv public_html_wp_upgrade/google* public_html/
rm -fr wordpress latest.zip
cd public_html;find -type f -exec chmod 644 {} \;
find . -type d -exec chmod 755 {} \;
find . -type f -exec chmod 644 {} \;

------
find . -name \*.htaccess -type f -delete
------

