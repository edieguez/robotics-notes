# Yubikey

## pam-u2f installation

```bash
sudo pacman -S pam-u2f
```

## Create configuration

```bash
mkdir -pv ~/.config/Yubico
pamu2fcfg -o pam://$(hostname) -i pam://$(hostname) > ~/.config/Yubico/u2f_keys
```

## Edit PAM configuration

```bash
# For sudo
sudo vi /etc/pam.d/sudo

# For login
sudo vi /etc/pam.d/login

# For sddm
sudo vi /etc/pam.d/sddm
```

Add the following line to the `auth` section. It must be before the `auth include system-auth` line.

```bash
auth sufficient pam_u2f.so cue origin=pam://$your_hostname appid=pam://$your_hostname
```

### Example

```text
#%PAM-1.0
# Yubikey support
auth        sufficient  pam_u2f.so  cue  origin=pam://pod-042a appid=pam://pod-042a

# Default auth methods
auth        include     system-auth
account     include     system-auth
session     include     system-auth
```
