# FFMPEG

## Get valid sources

``` bash
pactl list short sources
```

## Record system audio and microphone

``` bash
ffmpeg -y -f pulse -i 1 -f pulse -i 8 -filter_complex amix=inputs=2:duration=longest mix.mp3
```
