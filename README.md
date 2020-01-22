# NodeGoat

OWASP App to learn security issues on a node.js server: [NodeGoat](https://github.com/OWASP/NodeGoat)

## Getting Started

* Make sure you have Vagrant installed and ready to go.
* Make sure you have ansible installed.

Clone the repo:

``` bash
git clone https://github.comtjcim/nodegoat_vagrant && cd nodegoat_vagrant
```

Start the vagrant guest:

``` bash
vagrant up
```

## pm2

App uses pm2 to daemonize and start at boot. Run the following commands from the vagrant guest

Stop app
``` bash
pm2 stop server
```

restart App
``` bash
pm2 restart server
```

List apps
``` bash
pm2 list
```

Show logs of application
``` bash
pm2 logs server
```
