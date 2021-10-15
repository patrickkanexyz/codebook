---
title: How to fix 'The link you followed has expired' error
keywords: [wordpress]
copywrite: 
---
The error is caused by the file or theme you are trying to upload being larger
than the php server on the back end allows.

You can either edit the `php.ini` file, setting the variables below:
`memory_limit = 256M
upload_max_size = 64M
post_max_size = 64M
upload_max_filesize = 64M
max_execution_time = 300
max_input_time = 1000`

Or you can edit the `.htaccess` file in the Wordpress root directory.  This is
the prefered method, as it should work even on servers you don't have direct
control over, like shared hosting services.  Add the following into a new line
at the end of the file.
`php_value memory_limit 256M
php_value upload_max_filesize 64M
php_value post_max_size 64M
php_value max_execution_time 300
php_value max_input_time 1000`

After the edit refresh the page and it should work.  Also, don't edit these
variables to anything retarded like max uploads sizes of 1G.
