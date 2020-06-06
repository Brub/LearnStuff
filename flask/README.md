# Flask

[https://flask.palletsprojects.com/en/1.1.x/](https://flask.palletsprojects.com/en/1.1.x/)

## Install flask

```
pip install Flask
```

## voorbeeld programma

```python:
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
    return '<h1>Dag Bruno</h1>'

if __name__ == '__main__':
    app.run()
```