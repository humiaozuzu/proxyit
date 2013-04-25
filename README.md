Proxyit
=======

Proxy switcher for OS X

Principle
---------

The script uses `networksetup` change proxy for you.


Installation
------------

1. Copy `proxyit` to `/usr/local/bin`
2. Give `networksetup` superuser permissions to prevent it keeping asking password

``` bash
sudo chmod +s /usr/sbin/networksetup
```

Configs
-------

Example:

``` ini
[linode]
type=socks
host=192.168.1.1
port = 1018

[buyvm]
type=http
host=172.12.222.123
port=8101

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
