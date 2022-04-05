.htaccess Rewrite Rules:-
-------------------------

#Exclude the WP CRON and other scripts from authentication
<FilesMatch "(wp-cron.php|another-script.php)$">
Satisfy Any
Order allow,deny
Allow from all
Deny from none
</FilesMatch>

