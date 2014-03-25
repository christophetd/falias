#falias

Tired of having to type the full path of every config file you need to edit? Take a look at falias.

## Installation

```
sudo wget https://raw.githubusercontent.com/christophetd/falias/master/falias -O /usr/bin/falias
sudo chmod +x /usr/bin/falias
```

## Usage

_falias aliasname_ : 	Opens the file corresponding to 'aliasname' in the default editor, defined as the first found of : $EDITOR env variable, xdg-open, /usr/bin/editor, vim

_falias list_ :	Lists all aliases
	
_falias add aliasname filepath_ : Adds an alias named 'aliasname' corresponding to 'filepath'
	
_falias edit|update aliasname newFilepath_ : Updates the file corresponding to alias 'aliasname'
	
_falias remove|delete aliasname_ : Removes alias 'aliasname'
	
_falias flush_ : Removes all aliases (asks for confirmation)

* Relative file paths are converted to absolute ones.

* By default, falias data is stored in _/etc/falias.ini_, which has to be readable and writeable (but will be created automatically at first run) to the user running falias. You can change this path at the very beginning of the script.

## Example use

```
root@ubuntu-vm:~# falias add php /etc/php5/cli/php.ini 
Adding alias 'php <--> /etc/php5/cli/php.ini'

root@ubuntu-vm:~# falias add apache /etc/apache2/sites-available/default
Adding alias 'apache <--> /etc/apache2/sites-available/default'

root@ubuntu-vm:~# falias list
Alias php <--> /etc/php5/cli/php.ini
Alias apache <--> /etc/apache2/sites-available/default

root@ubuntu-vm:~# falias php
(opens /etc/php5/cli/php.ini in gedit)
```

## Author

Feel free to send me any remarks / requests via email (christophe.tafani.dereeper@epfl.ch) or [via twitter](http://twitter.com/christophetd).
