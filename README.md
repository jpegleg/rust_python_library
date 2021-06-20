# rust_python_library
use compiled rust as a python library

Example flask app that imports rust_python_module_example.so, which is just an example that returns a string.

```
from flask import Flask

import rust_python_module_example

app = Flask(__name__)

@app.route('/')
def main():
    return rust_python_module_example.get_result('Hello!')
```
