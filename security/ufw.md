# [Uncomplicated Firewall (ufw)](https://itsfoss.com/ufw-ubuntu)

## Installation

> `plasma-firewall` is a GUI for `ufw` and is not required.

``` shell
pacman -S ufw plasma-firewall
# or
yay -S ufw plasma-firewall
```

## `ufw` general commands

``` shell
ufw version

sudo ufw status

sudo ufw enable
sudo ufw disable

sudo ufw reset # reset to default settings
sudo ufw reload # reload rules
```

## Default recommended rules

``` shell
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

## View added rules

``` shell
sudo ufw show added
```

## [Allow incoming traffic](https://learnubuntu.com/allow-port-firewall)

> All these commands do the same: allow SSH traffic through port 22

``` shell
sudo ufw allow 22
sudo ufw allow 22/tcp
sudo ufw allow ssh
```

## [Delete rules](https://learnubuntu.com/allow-port-firewall/#how-to-delete-ufw-rules-in-ubuntu)

``` shell
sudo ufw status numbered # take note of the $rule_number
sudo ufw delete $rule_number
```
