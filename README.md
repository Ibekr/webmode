# webmode
A simple script to set up user and group permissions for webserver's directories (and all sub directories).

Gives permissions:
 * **760** (- rwx rw- ---) for all files in directory and subdirectories
 * **770** (d rwx rwx ---) for directory and all subdirectories recursively

As a default, it gives permissions to **www-data** user and **www-data** group.

An example of use:
~~~~
webmode.sh /var/www/example.com/
~~~~

Repo:
https://github.com/Ibekr/webmode/blob/master/README.md
