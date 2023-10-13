# Azure Web App: Flask
Flask is a lightweight framework (python library) for web development
- This document will cover some fundamentals for setting up a web app

## app.py
This is (by default) the main entry point for the web app
- Before creating, see:
  - GitHub - setup a repository
  - Conda - setup a conda environment for local development (and create the requirements.txt file)

Here is a very simple example I use to just test the basic setup of my web app:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def index():
    return "Hello world"
```

