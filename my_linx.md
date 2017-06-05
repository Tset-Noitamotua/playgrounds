# My Linux (Debian / Ubuntu) Configuration


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
