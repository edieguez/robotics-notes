# Using SSH as SOCKS proxy

## Dynamic port forwarding

```bash
ssh -fCND $port $username@$ssh_server
```

- `-f` - go to background
- `-C` - compress data
- `-N` - do not execute a remote command
- `-D` - dynamic port forwarding
