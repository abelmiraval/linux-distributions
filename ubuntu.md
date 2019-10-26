# Settings

GNOME Tweaks

User themes

Dash to Dock

# Themme,icon

Communitheme

$ sudo add-apt-repository ppa:dyatlov-igor/la-capitaine
$ sudo apt-get install la-capitaine-icon-theme

# Zsh

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

\$ chmod 755 xampp-linux-x64-7.2.21-1-installer.run

\$ ls -l xampp-linux-x64-7.2.21-1-installer.run

\$ sudo ./xampp-linux-x64-7.2.21-1-installer.run

\$ sudo /opt/lampp/lampp start

# Composer

\$ sudo curl -s https://getcomposer.org/installer | /opt/lampp/bin/php

\$ sudo ln -s /opt/lampp/bin/php /usr/local/bin/php

\$ sudo mv composer.phar /usr/local/bin/composer

# XDEBUG

Abra su navegador y obtenga la salida de phpinfo () ; copie y pegue todo el código fuente HTML en el área de texto del Asistente Xdebug https://xdebug.org/wizard

Descargue la fuente comprimida .tgz

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

# ssh

\$ mkdir ~/.ssh

\$ cd ~/.ssh

\$ ssh-keygen -t rsa -b 4096

\$ eval `ssh-agent -s`

\$ sudo ssh-add /home/<your username>/.ssh/id_rsa

\$ cat ~/.ssh/id_rsa.pub
-Configurate ssh github

\$ git config --global user.name "<your username>"

\$ git config --global user.email your@email.com

# Mongodb

\$ sudo apt update

Now install the MongoDB package itself:
\$ sudo apt install -y mongodb
