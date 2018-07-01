# zenphoto-adminarea-protect
protect the zenphoto admin area with htaccess htpasswd

For additional protection of the admin area at ZenPhoto, a `.htaccess` `.htpasswd` password protection can be created.

To do this, a file `.htaccess` and a file `.htpasswd` is needed and must be created in the `/zp-core/` folder.

The contents of the files are published here for an example in the folder `/zp-core/`.

The user and the password can be generated via command line and changed at any time.

first, go into the folder /zp-core/   
`cd /var/www/virtual/user/html/zp-core/`

for SHA:   
`htpasswd -bs .htpasswd username password`

for bcrypt   
`htpasswd -bB .htpasswd username password`

ATTENTION: Please use only ASCII Signs for username and password.

When calling the following URLs, the Apache server takes password protection.
   
`example.com/admin.php`   
`example.com/zp-core/admin.php`   
`example.com/zp-core/admin-{whatever}.php`   
  
