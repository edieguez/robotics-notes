# SSH

## Config file

The SSH configuration file is located at `~/.ssh/config`

- Use the options you need. Usually, you will need to set the `HostName` and `User`
- Not all options can be set in the config file. For a complete list of options, see `man ssh_config`.

```properties
Host targaryen-house
    HostName 192.168.1.10
    User daenerys
    Port 7654
    IdentityFile ~/.ssh/targaryen.key
    LogLevel INFO
    Compression yes
```

## Reference

- [Using the SSH Config File](https://linuxize.com/post/using-the-ssh-config-file)
