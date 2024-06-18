---
id: 0bip38suxyqbtq3kp8e44gd
title: Flask
desc: ''
updated: 1717512036101
created: 1717511815693
---

The file that flask run by default is `app.py` or `wsgi.py`

### app.py
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "Hello World"

@app.route('/<name>')
def hello(name: str):
    return f"Hello {name}"

if __name__ == '__main__':
    app.run()
```

### To run it

**Way 1:**
```bash
python app.py
```

**Way 2:**
```bash
flask run
```

> #### Now if you give any other name than `app.py` then you'll have to run it either using *way-1* or using:
- Name of file : `index.py`
```bash
flask --app index run
```