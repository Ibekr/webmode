# webmode
A simple script to set up user and group permissions for webserver's directories

~~~~
#!/bin/bash

if [ "$1" == "" ]; then
        echo 'parameter is empty. Example: webmod.sh /var/www/' 1>&2
        exit 1
fi

# Make sure only root can run our script
if [ "$(id -u)" != "0" ]; then
   echo "This script must be run as root" 1>&2
   exit 1
fi

chown -R www-data:www-data "$1"
chmod u=rwx,g=rw,o= -R "$1"
find "$1" -type d -exec chmod g+x {} \;

~~~~

