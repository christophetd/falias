#falias

Tired of having to type the full path of every config file you need to edit? Take a look at falias.

## Usage

falias aliasname 
	Opens the file corresponding to 'aliasname' in the default editor, defined as the first found of : $EDITOR env variable, xdg-open, /usr/bin/editor, vim

falias list
	Lists all aliases
	
falias add aliasname filepath
	Adds an alias named 'aliasname' corresponding to 'filepath'
	
falias edit|update aliasname newFilepath
	Updates the file corresponding to alias 'aliasname'
	
falias remove|delete aliasname
	Removes alias 'aliasname'
	
falias flush
	Removes all aliases (asks for confirmation)

Relative file paths are converted to absolute ones.

By default, falias data is stored in /etc/falias.ini, which has to be readable and writeable (but will be created automatically at first run). You can change this path at the very beginning of the script.

## Example use

```
root@ubuntu-vm:/home/christophe# falias add php /etc/php5/cli/php.ini 
Adding alias 'php <--> /etc/php5/cli/php.ini'

root@ubuntu-vm:/home/christophe# falias add apache /etc/apache2/sites-available/default
Adding alias 'apache <--> /etc/apache2/sites-available/default'

root@ubuntu-vm:/home/christophe# falias list
Alias php <--> /etc/php5/cli/php.ini
Alias apache <--> /etc/apache2/sites-available/default

root@ubuntu-vm:/home/christophe# falias php
(opens /etc/php5/cli/php.ini in gedit)
```

## Author

Feel free to send me any remarks / requests via email (christophe.tafani.dereeper@epfl.ch) or [via twitter](http://twitter.com/christophetd).
