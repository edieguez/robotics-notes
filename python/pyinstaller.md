# [PyInstaller](https://pyinstaller.org/en/stable/)

Compiles a Python script into an executable binary

> The project is compressed into a single file. During execution is decompressed in the temporary folder. If you have operations dependant on the binary base dir this option is almost not usable

```shell
pip install pyinstaller

pyinstaller --onefile $path/to/script.py
```
