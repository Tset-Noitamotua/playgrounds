# My Linux (Debian / Ubuntu) Configuration

- Python 3.6 (incl. PIP)
- opt. PIP for Python 2.7
- GIT
- VirtualenvWrapper
- RF, RF-DebugLibrary, ...
- S2L
- Packer, Vagrant, Docker, VirtualBox
- ATOM, plugins
- VSCode, plugis


Python 3.6 install
------------------

```shell
# build from source
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
cd ~/Downloads
wget https://www.python.org/ftp/python/3.6.1/Python-3.6.1.tar.xz
sudo tar -xzf Python-3.6.1.tar.xz
cd Python-3.6.1
sudo ./configure
sudo make altinstall
## add an alias for pip to your .bashrc
# alias pip='python3.6 -m pip'
## add pip list format to .bashrc
# export PIP_FORMAT=columns
```


VirtualBox install
------------------
```shell
sudo apt install virtualbox
sudo apt install virtualbox-ext-pack
# for Guest OS --> sudo apt install virtualbox-guest-additions-iso
# CHECK: vboxmanage --version
```


Google Chrome install
---------------------

```shell
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable
# sudo apt-get install google-chrome-beta           # BETA Version
# sudo apt-get install google-chrome-unstable # UNSTALBLE Version
# CHECK: google-chrome-stable --version
```


Chrome WebDriver (Chromedriver) install
---------------------------------------

```shell
sudo apt install chromedriver
# CHECK: chromedriver --version
```

FireFox WebDriver (Geckodriver) install
---------------------------------------
```shell
cd ~/Downloads
wget https://github.com/mozilla/geckodriver/releases/download/v0.16.1/geckodriver-v0.16.1-linux64.tar.gz
tar -xvzf geckodriver*
chmod +x geckodriver
sudo mv geckodriver /usr/local/bin/
rm geckodriver-v0.16.1-linux64.tar.gz
# CHECK: geckodriver --version
```
