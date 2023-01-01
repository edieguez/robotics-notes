# [Jinja2](https://jinja.palletsprojects.com)

## Installation

``` bash
pip install jinja2
```

## [Usage](https://jinja.palletsprojects.com/templates)

```python
from jinja2 import Environment, FileSystemLoader

env = Environment(loader=FileSystemLoader('templates'))
template = env.get_template('index.html')
context = {
    'title': 'Hello World',
    'content': 'This is a content'
}

print(template.render(context))
```
