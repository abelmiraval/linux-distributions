# Install Software

	- GNOME Tweaks

	- User themes

	- Dash to Dock

# Themme, Icon

## Communitheme

	$ sudo add-apt-repository ppa:dyatlov-igor/la-capitaine

	$ sudo apt-get install la-capitaine-icon-theme

# SSH

	$ git config --global user.name "<yourusername>"

	$ git config --global user.email "<your@email.com>"

	$ mkdir ~/.ssh

	$ cd ~/.ssh

	$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

	$ eval ssh-agent -s

	$ ssh-add ~/.ssh/id_rsa

	$ cat ~/.ssh/id_rsa.pub

	- Add the SSH key to your GitHub account.

# NVM

	- cd ~/ from anywhere then 
	
	- git clone https://github.com/nvm-sh/nvm.git .nvm

	- Now add these lines to your ~/.zshrc

		export NVM_DIR="$HOME/.nvm"
		[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
		[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

	- nvm install v12.18.4

	- nvm list

	- nvm use v12.18.2

	- node -v

# Yarn

	$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

	$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

	$ sudo apt update

	$ sudo apt install yarn

# ZSH

	$ sudo apt install git-core zsh

	$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

	$ sudo apt install fonts-powerline

	$ nano ~/.zshrc

	- Find the ZSH_THEME variable and change it:ZSH_THEME="agnoster"

	$ cd ~/.oh-my-zsh/themes

	$ nano agnoster.zsh-theme

	- Now we can change the ‘Main prompt’. We don’t need to prompt_context in the function build_prompt().
	  Just comment out this line or remove it.

	$ source ~/.zshrc

	$ chsh -s $(which zsh)

	$ logout

	$ zsh

	$ nano ~/.zshrc

	- plugins=(git colored-man-pages)

	$ source ~/.zshrc

	$ cd ~/.oh-my-zsh/custom/plugins

	$ git clone https://github.com/zsh-users/zsh-syntax-highlighting

	- plugins=(git colored-man-pages zsh-syntax-highlighting)

	$ git clone https://github.com/zsh-users/zsh-autosuggestions

	- plugins=(git colored-man-pages zsh-syntax-highlighting zsh-autosuggestions)

# Heroku

	$ wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh

	$ nano ~/.zshrc

	- plugins=(git heroku)

	$ heroku login

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

	- Install pgAdmin III

# Mongodb

	$ sudo apt update

	- Now install the MongoDB package itself:

	$ sudo apt install -y mongodb

# Xampp

	- Dowloand xampp https://www.apachefriends.org/download.html

	$ chmod 755 xampp-linux-x64-7.2.21-1-installer.run

	$ ls -l xampp-linux-x64-7.2.21-1-installer.run

	$ sudo ./xampp-linux-x64-7.2.21-1-installer.run

	$ sudo /opt/lampp/lampp start

# Composer

	$ sudo curl -s https://getcomposer.org/installer | /opt/lampp/bin/php

	$ sudo ln -s /opt/lampp/bin/php /usr/local/bin/php

	$ sudo mv composer.phar /usr/local/bin/composer

	$ sudo chown -R <user> /home/<user>/.composer/cache/

# NodeJS

	$ sudo apt update

	$ sudo apt install nodejs

	$ sudo apt install npm

	$ nodejs -v

# Visual Code

## Extension

### Settings

	- Prettier

	- Bracket Pair Colorizer

	- Material Icon Theme

	- Auto Rename Tag

	- Live Server

	- DotENV

	- Path Intellisense

	- Project Manager

### Theme

	- Code Blue

	- Horizon Theme

### php

	- PHP Debug

	- PHP Intelphense

	- PHP IntelliSense

	- PHP Namespace Resolver

### Laravel

	- Laravel Extension Pack

### Vue

	- Vetur

	- Vue 2 Snippets

	- Vuetify vscode

## Xdebug

	- phpinfo () copy and pase all the source code HTML in Xdebug https://xdebug.org/wizard

	- Dowloand the file .tgz

	$ sudo tar -xvzf xdebug-2.2.1.tgz

	$ cd xdebug-2.2.1

	$ sudo apt update

	$ sudo apt install php7.2-dev

	$ phpize

	$ sudo ./configure -enable-xdebug --with-php-config=/opt/lampp/bin/php-config

	$ sudo make

	$ sudo cp modules/xdebug.so /opt/lampp/lib/php/extensions/no-debug-non-zts-20170718

	- Edit the file /opt/lampp/etc/php.ini and add line:

		[zend]
		zend_extension="/opt/lampp/lib/php/extensions/no-debug-non-zts-20170718/xdebug.so"

		[XDebug]
		xdebug.remote_enable = 1
		xdebug.remote_autostart = 1

	$ sudo /opt/lampp/lampp restart

# Sublime Text 3

## Install

	$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -

	$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

	$ sudo apt-get update

	$ sudo apt-get install sublime-text

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

## php

	$ sudo ln -s /opt/lampp/bin/php /usr/bin/php

## neofetch

	$ sudo add-apt-repository ppa:dawidd0811/neofetch

	$ sudo apt update && sudo apt install neofetch

	$ neofetch


# Ruby install

	$ sudo apt-get install build-essential

	$ wget -O ruby-install-0.7.0.tar.gz \https://github.com/postmodern/ruby-install/archive/v0.7.0.tar.gz

	$ tar -xzvf ruby-install-0.7.0.tar.gz

	$ cd ruby-install-0.7.0/

	$ sudo make install

	$ ruby-install -V

# Ruby

	$ ruby-install ruby 2.6.6

	$ wget -O chruby-0.3.9.tar.gz \https://github.com/postmodern/chruby/archive/v0.3.9.tar.gz

	$ tar -xzvf chruby-0.3.9.tar.gz

	$ cd chruby-0.3.9/

	$ sudo make install

	$  cat >> ~/.$(basename $SHELL)rc <<EOF source /usr/local/share/chruby/chruby.sh source /usr/local/share/chruby/auto.sh EOF

	$ exec $SHELL

	$ echo "ruby-2.6.6" > ~/.ruby-version

	$ source ~/.zshrc

	$ chruby ruby-2.6.6

	$ ruby -v

# Rails

	$ gem install rails -v 6.0.0 -N

# Sqlite3

	$ echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

	$ sudo apt-get install sqlite3 libsqlite3-dev

# PostgreSQL

	$ sudo apt-get install libpq-dev

# Bundler

	$ gem install bundler

# App

	$ rails new my_app_name --database=postgresql

	$ bundler install

# Multimedia
	
	Zoom

	Anydesk

	Postman

	Insommia
	
	Discord
	
	WoeUsb

	KRDC

	simplescreenrecorder

	Tilix
	- Now add these lines to your ~/.zshrc

	if [ $TILIX_ID ] || [ $VTE_VERSION ]; then
		source /etc/profile.d/vte-2.91.sh
	fi

