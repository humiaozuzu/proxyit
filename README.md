Proxyit
=======

Proxy changer for OS X

Principle
---------

The script uses `networksetup` change proxy for you.


Installation
------------

1. Copy `proxyit` to `/usr/local/bin`
2. Give `networksetup` superuser permissions to prevent it keep asking password
``` bash
sudo chmod +s /usr/sbin/networksetup
```

Configs
-------

Example:

``` ini
[linode]
type=socks
host=172.18.184.217
port = 1088

[buyvm]
type=http
host=172.18.184.111
port=8501

[mal]
type=pac
url=http://10.0.1.44/x.pac
```

Put it in `~/.proxyit`

Usage
-----

``` bash
$ proxyit list       # list all available proxy settings
linode buyvm mal

$ proxyit set linode # use linode proxy setting

$ proxyit unset      # unset all proxy settings
```
