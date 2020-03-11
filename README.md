## Ubuntu Development Setup

#### <u>Update</u>

```bash
$ sudo apt-get update && apt-get upgrade
$ sudo apt-get install software-properties-common
```

***

#### <u>Useful Packages</u>

```bash
$ sudo apt-get install curl wget htop nmap traceroute tmux unzip vim make ack silversearcher-ag mtr pydf lftp aria2 nnn libssl-dev libreadline-dev zlib1g-dev clang gcc-multilib build-essential libffi-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libffi-dev libusb-1.0-0-dev libudev-dev libpulse-dev exfat-fuse exfat-utils cmake pkg-config libgtk-3-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev libjpeg-dev libpng-dev libtiff-dev gfortran openexr libtbb2 libtbb-dev libdc1394-22-dev autoconf bison libyaml-dev ca-certificates
```

```bash
$ sudo apt-get install python3-dev python-dev python3-pip python-pip python3-setuptools python-setuptools
```

```bash
$ sudo pip3 install thefuck
```

***

#### <u>Git</u> 

```bash
$ sudo apt-get install git git-core
$ git config --global user.name "Your Name"
$ git config --global user.emai "Your Email"
$ git config --global color.ui auto
```

***

#### <u>Mercurial</u>

```bash
$ sudo apt-get install mercurial
```

***

#### <u>Subversion</u>

```bash
$ sudo apt-get install subversion
```

***

#### <u>Zsh</u>

```bash
$ sudo apt-get install zsh
```

***

#### <u>Oh My Zsh</u>

via curl:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

via wget:

```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Plugins:

```bash
$ cd ~/.oh-my-zsh/custom/plugins
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting
$ git clone https://github.com/zsh-users/zsh-autosuggestions
```

Add `zsh-syntax-highlighting`, `zsh-autosuggestions`, `colored-man-pages` in `~/.zshrc` under plugins.

```bash
$ source ~/.zshrc
```

***


#### <u>Fonts</u>

```bash
$ sudo apt-get install ttf-mscorefonts-installer
$ sudo apt-get install fonts-powerline
```

***

#### <u>Generate SSH Keys</u>

```bash
$ ssh-keygen -o -a 256 -t ed25519
```

To copy public key to a particular server, user `ssh-copy-id <user@hostname>`

To setup GitHub, copy and paste SSH key into GitHub website. Use `pbcopy < ~/.ssh/id25519.pub` to clipboard.

To verify, `ssh -T git@github.com`. You should get a message "Successfully Authenticated". You should be able to push/pull from your remote GitHub repo using SSH URL. 

***

#### <u>Python 3</u>

To see which version of Python 3 your have installed, run

```bash
$ python3 --version
$ sudo apt-get update
$ sudo apt-get install python3.8
$ sudo apt-get install python3-dev
$ sudo apt-get install -y python3-pip
$ sudo apt-get install python3-numpy
```

Python packages can be installed by typing:

```bash
$ pip3 install <package_name>
```

***

#### <u>Apache</u>

```bash
$ sudo apt-get install apache2
```

***

#### <u>MySQL</u>

```bash
$ sudo apt-get install mysql-server
$ sudo mysql_secure_installation
```

```bash
$ sudo mysql -u root -p
```

***

#### <u>PHP</u>

```bash
$ sudo apt-get install php libapache2-mod-php php-mysql
$ sudo apt-get install phpmyadmin
$ sudo ln -s /etc/phpmyadmin/apache.conf /etc/phpmyadmin/conf.d/phpmyadmin.conf
$ sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
```

***

#### <u>Ruby</u>

```bash
$ sudo apt-get update
$ curl -sL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-installer | bash -
$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
$ echo 'eval "$(rbenv init -)"' >> ~/.zshrc
$ source ~/.zshrc
$ rbenv install -l
$ rbenv install 2.7.0
$ rbenv global 2.7.0
$ ruby -v
```

```bash
$ sudo apt-get install rubygems
$ gem install sass
$ gem install compass
```

***

#### <u>Java 8</u>

```bash
$ sudo apt-get update
$ sudo apt-get install openjdk-8-jdk openjdk-8-jre
$ java -version
```

***

#### <u>Node.js</u>

```bash
$ sudo apt-get install nodejs
$ sudo apt-get install npm
$ nodejs -v
```

***

#### <u>Docker</u>

```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
$ sudo apt-get install docker-ce
$ sudo systemctl status docker
$ sudo usermod -aG docker ${USER}
$ su - ${USER}
$ id -nG
$ sudo usermod -aG docker <username>
```

***

#### <u>AWS CLI</u>

```bash
$ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
$ unzip awscliv2.zip
$ sudo ./aws/install
$ aws --version
```

***

