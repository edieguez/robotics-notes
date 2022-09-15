# [zipapp](https://docs.python.org/3.10/library/zipapp.html)

Generates an executable (compressed in zip) file for Python projects

## Usage

### Install PIP dependencies

``` shell
python -m pip install -r $app_dir/requirements.txt --target $app_dir
```

### Generate compressed binary

``` shell
python -m zipapp --compress --python '/usr/bin/env python' $app_dir
```
