# trap

## Get list of available signals

```bash
trap -l

# For ZSH
bash -c "trap -l"
```

## Ignore signals

```bash
trap '' HUP
```

## Run a command when a signal is received

> `EXIT` is a pseudo signal that is run when the shell exits

```bash
# Trap CTRL+C
trap 'echo "CTRL+C pressed"' INT

# Will run when the script finishes
trap 'echo "Signal received"' EXIT
```
