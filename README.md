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

In the docker_example directory, there is a template for building a docker image based on rust docker image, running the python app inside it.
