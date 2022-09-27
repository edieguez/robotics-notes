# Loopback audio device

Redirect desktop audio to any output device. Install `pavucontrol` to define the inputs for the null sink device

## Add null sink

``` shell
# Set up the mixed sound sink
pactl load-module module-null-sink sink_name=LoopSink

# Set up the first loopback sink
pactl load-module module-loopback sink=LoopSink

# Set up the second loopback sink
pactl load-module module-loopback sink=LoopSink
```

## Deactivate null sink

``` shell
pactl unload-module module-null-sink
pactl unload-module module-loopback sink=LoopSink
```
