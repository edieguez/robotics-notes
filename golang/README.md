# Go language

## Custom installation

- Download the latest version of Go from the [official website](https://golang.org/dl)
- Extract the archive to `/opt/go`
- Add the following environment variables

```bash
export GOROOT=/opt/go
export GOPATH=$GOROOT/gopath
```

- Add Go to your PATH variable. You need to edit your `.bashrc` or `.zshrc`

```bash
export PATH+=":$GOROOT/bin"
```
