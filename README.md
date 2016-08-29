# CI_htaccess
Remove "index.php" from CodeIgniter URL


## Three Easy Steps:

1. Make sure you remove "index.php" from $config['index_page'] = '' in application/config/config.php
2. Create a new file in root ".htaccess" by using any code editor.
3. Add the following code and Save it:

```code
RewriteEngine on
RewriteCond $1 !^(index\.php|public|\.txt)
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php?$1


