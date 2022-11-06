# Hardening

## Audit system for hardening suggestions

``` shell
sudo lynis audit system
```

## Firewall

Install `plasma-firewall` and `ufw`

## Rootkit scanner

Install `rkhunter` and perform a scan

``` shell
sudo rkhunter --check --sk
```

## Package auditing tool

Install `arch-audit` and perform a scan

``` shell
arch-audit
```
