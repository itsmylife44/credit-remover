OpenEthereumPool Credit Remover
===============================

 
 credits esn

### Install NodeJS
    $ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
    $ sudo apt-get install nodejs

### Copy source file
    $ cd /root
    $ git clone https://github.com/itsmylife44/credit-remover
    $ cd credit-remover
    $ mkdir backup

### Install Dependence
    $ npm install redis
    $ npm install system-sleep
    $ npm install isnumber

### Config
    $ vi config.json
    $
    $   {
    $       "coin": "eth",
    $       "aliveBlocks": 10000,
    $       "redisPool": {
    $           "host": "127.0.0.1",
    $           "port": 6379,
    $           "password": ""
    $       },
    $       "backup": true,
    $       "backupPath": "/root/credit-remover/backup/"
    $   }
    $
    $ coin
    $ redis 
    $ aliveBlocks 
    $ backup 
    $ backupPath

### Run
    $ node init.js

### Use crontab
    $ crontab -e
    $ 0 0 * * * node /root/credit-remover/init.js >> /root/credit-remover/remover.log
