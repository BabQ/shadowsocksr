wget http://www.djangoz.com/ssr

sudo mv ssr /usr/local/bin

sudo chmod 766 /usr/local/bin/ssr

ssr install

ssr config

sudo apt-get install polipo

sudo gedit /etc/polipo/config
------------------------------------
logSyslog = false
logFile = "/var/log/polipo/polipo.log"
socksParentProxy = "127.0.0.1:1080"
socksProxyType = socks5
chunkHighMark = 50331648
objectHighMark = 16384
serverMaxSlots = 64
serverSlots = 16
serverSlots1 = 32
proxyAddress = "0.0.0.0"
proxyPort = 8123
-------------------------------------

/etc/init.d/polipo restart

echo "export http_proxy="http://127.0.0.1:8123/"">>~/.bashrc
