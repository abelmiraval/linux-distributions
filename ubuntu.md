# Install software

GNOME Tweaks

User themes

Dash to Dock

# Themme, icon

Communitheme

\$ sudo add-apt-repository ppa:dyatlov-igor/la-capitaine

\$ sudo apt-get install la-capitaine-icon-theme

# ZSH

\$ sudo apt install git-core zsh

$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

\$ sudo apt install fonts-powerline

\$ nano ~/.zshrc

-Find the ZSH_THEME variable and change it:ZSH_THEME="agnoster"

\$ cd ~/.oh-my-zsh/themes

\$ nano agnoster.zsh-theme

-Now we can change the ‘Main prompt’. We don’t need to prompt_context in the function build_prompt(). Just comment out this line or remove it.

\$ source ~/.zshrc

$ chsh -s $(which zsh)

-logout

\$ zsh

\$ nano ~/.zshrc

- plugins=(git colored-man-pages)

\$ source ~/.zshrc

$ cd ~/.oh-my-zsh/custom/plugins

$ git clone https://github.com/zsh-users/zsh-syntax-highlighting

- plugins=(git colored-man-pages zsh-syntax-highlighting)

\$ git clone https://github.com/zsh-users/zsh-autosuggestions

- plugins=(git colored-man-pages zsh-syntax-highlighting zsh-autosuggestions)

# Heroku

\$ wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh

\$ nano ~/.zshrc

plugins=(git heroku)

\$ heroku login

# Xammp

 Dowloand xampp https://www.apachefriends.org/download.html

\$ chmod 755 xampp-linux-x64-7.2.21-1-installer.run

\$ ls -l xampp-linux-x64-7.2.21-1-installer.run

\$ sudo ./xampp-linux-x64-7.2.21-1-installer.run

\$ sudo /opt/lampp/lampp start

# Postgresql

 $ sudo apt-get install wget ca-certificates

 $ wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

 $ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'

 $ sudo apt-get update

 $ sudo apt-get install postgresql postgresql-contrib

 $ sudo su - postgres

 $ psql

 $ \conninfo

 $ sudo -u postgres psql

 $ \password

  Install pgAdmin III

# Composer

\$ sudo curl -s https://getcomposer.org/installer | /opt/lampp/bin/php

\$ sudo ln -s /opt/lampp/bin/php /usr/local/bin/php

\$ sudo mv composer.phar /usr/local/bin/composer

# ssh

\$ git config --global user.name "<yourusername>"

\$ git config --global user.email "<your@email.com>"

\$ mkdir ~/.ssh

\$ cd ~/.ssh

\$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

\$ eval ssh-agent -s

\$ ssh-add ~/.ssh/id_rsa

\$ cat ~/.ssh/id_rsa.pub

 Agregue la clave SSH a su cuenta de GitHub .

# Yarn
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

$ sudo apt update

$ sudo apt install yarn

# vs code


# Sublime Text 3

	## Extension

	- ctrl + shift => Install package manager
	- Laravel blade Highligther
	- PHP companion
	- A file icon
	- Sass
	- Vue Complete Package

	## Key Binds

	{ "keys": ["ctrl+b"], "command": "toggle_side_bar" },

	{ "keys": ["f6"], "command": "expand_fqcn" },

	{ "keys": ["shift+f6"], "command": "expand_fqcn", "args": {"leading_separator": true} },

	{ "keys": ["f5"], "command": "find_use" },

	{ "keys": ["f4"], "command": "import_namespace" },

	{ "keys": ["f3"], "command": "implement" },

	{ "keys": ["shift+f12"], "command": "goto_definition_scope" },

	{ "keys": ["f7"], "command": "insert_php_constructor_property" }

	## Settings

	"color_scheme": "Packages/Material Theme/schemes/Material-Theme-Darker.tmTheme",

	"font_size":16,

	"font_face": "Fira code",

	"ignored_packages":
	[
		"Vintage"
	],

	"theme": "Material-Theme-Darker.sublime-theme",

	"save_on_focus_lost": true,

	"trim_trailing_white_space_on_save": true,

	"line_padding_top": 6,

    "line_padding_bottom": 8,

# Global Commands
 - $ sudo ln -s /opt/lampp/bin/php /usr/bin/php

# xdebug

phpinfo () copy and pase all the source code HTML in Xdebug https://xdebug.org/wizard

Dowloand the file .tgz

\$ sudo tar -xvzf xdebug-2.2.1.tgz

\$ cd xdebug-2.2.1

\$ sudo apt update

\$ sudo apt install php7.2-dev

\$ phpize

\$ sudo ./configure -enable-xdebug --with-php-config=/opt/lampp/bin/php-config

\$ sudo make

\$ sudo cp modules/xdebug.so /opt/lampp/lib/php/extensions/no-debug-non-zts-20170718

Edit the file /opt/lampp/etc/php.ini and add line:

[zend]
zend_extension="/opt/lampp/lib/php/extensions/no-debug-non-zts-20170718/xdebug.so"

[XDebug]
xdebug.remote_enable = 1
xdebug.remote_autostart = 1

\$ sudo /opt/lampp/lampp restart

# NodeJS

\$ sudo apt update

\$ sudo apt install nodejs

\$ sudo apt install npm

\$ nodejs -v


# Mongodb

\$ sudo apt update

Now install the MongoDB package itself:
\$ sudo apt install -y mongodb
