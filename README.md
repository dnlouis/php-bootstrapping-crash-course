php-bootstrapping-crash-course
==============================

This is the example code used in the Binpress Tutorial *A PHP bootstrapping crash course* written by Vito Tardia. Read it here: https://www.binpress.com/tutorial/php-bootstrapping-crash-course/146

It can be a chore to manage script dependencies as your PHP applications grow larger and more complex. Once you've finished this crash course in bootstrapping, you'll have a basic -- yet powerful -- modern application template with simplified script dependency built in.

<buckAngus 08/22/2016>
I had trouble getting the index.php routing to work.  The following link got me over that hurdle.
  - http://help.slimframework.com/discussions/problems/10216-beginner-routes-not-working
  - Added the following to “000-default.conf” (virtual host file):
    - \<Directory "/var/www/[your_URI_path to]/public/"\>
    -   AllowOverride All 
    -   Order allow,deny 
    -   Allow from all 
    - \</Directory\>
  
  - And added the following to my setup script
    - sudo a2enmod rewrite
    - Then (of course): sudo service apache2 restart
</buckAngus>
