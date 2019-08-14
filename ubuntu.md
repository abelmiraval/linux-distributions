1. Settings
   
GNOME Tweaks
User themes
Dash to Dock

2. Themme,icon
   
communitheme
$ sudo add-apt-repository ppa:dyatlov-igor/la-capitaine
$ sudo apt-get install la-capitaine-icon-theme

3. Zsh

$ sudo apt install git-core zsh

$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

$ sudo apt install fonts-powerline

$ nano ~/.zshrc

-Find the ZSH_THEME variable and change it:ZSH_THEME="agnoster"

$ cd ~/.oh-my-zsh/themes

$ nano agnoster.zsh-theme

-Now we can change the ‘Main prompt’. We don’t need to prompt_context in the function build_prompt(). Just comment out this line or remove it. 

$ source ~/.zshrc

$ chsh -s $(which zsh)

-logout

$ nano ~/.zshrc
- plugins=(git colored-man-pages)

$ source ~/.zshrc

$ cd ~/.oh-my-zsh/custom/plugins
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting

- plugins=(git colored-man-pages zsh-syntax-highlighting)

$ git clone https://github.com/zsh-users/zsh-autosuggestions

- plugins=(git colored-man-pages zsh-syntax-highlighting zsh-autosuggestions)



4. Heroku

$ wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh

$ nano ~/.zshrc
    plugins=(git heroku)

$ heroku login

5. Xammp

$ chmod 755 xampp-linux-x64-7.2.21-1-installer.run
$ ls -l xampp-linux-x64-7.2.21-1-installer.run
$ sudo ./xampp-linux-x64-7.2.21-1-installer.run
$ sudo /opt/lampp/lampp start
   

6. Composer

$ sudo curl -s https://getcomposer.org/installer | /opt/lampp/bin/php

$ sudo ln -s /opt/lampp/bin/php /usr/local/bin/php

$ sudo mv composer.phar /usr/local/bin/composer


7. NodeJS

$ sudo apt update
$ sudo apt install nodejs
$ sudo apt install npm
$ nodejs -v


8. ssh

$ mkdir ~/.ssh

$ cd ~/.ssh

$ ssh-keygen -t rsa -b 4096

$ eval `ssh-agent -s`

$ sudo ssh-add /home/<your username>/.ssh/id_rsa

$ cat ~/.ssh/id_rsa.pub
-Configurate ssh github

$ git config --global user.name "<your username>" 

$ git config --global user.email your@email.com



9. Command

