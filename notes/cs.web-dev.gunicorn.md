---
id: 34d45i13jwal0by7pcbmcqz
title: Gunicorn
desc: ''
updated: 1717519605558
created: 1717512526583
---

### Run `flask` app in `gunicorn`

File name : `index.py` which has the app

*index.py:*
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

*To run it:*
```
gunicorn index:app
```

## Options
1. You can specify the host and port using the `-b` flag. For example, to run Gunicorn on `127.0.0.1:5000`, use:
> ```bash
> gunicorn index:app -b localhost:5000
> ```

2. Workers  
workers refer to the individual processes or threads that handle incoming requests and serve the web application. Each worker operates independently and can handle multiple requests simultaneously.

> The default no of workers is *1*

Use `-w` or `--workers` to set them :

*Ex:*
```bash
gunicorn --workers=11 wrlogs:app -b localhost:5000
```

## Problems
#### Gunicorn not using the venv in `sudo`

```bash
localdisk/hg/Python-Projects/gunicorn-flask via 🐍 v3.11.5 (venv) took 6m14s 
❯ gunicorn index:app
[2024-06-04 22:15:05 +0530] [459677] [INFO] Starting gunicorn 22.0.0
[2024-06-04 22:15:05 +0530] [459677] [INFO] Listening at: http://127.0.0.1:8000 (459677)
[2024-06-04 22:15:05 +0530] [459677] [INFO] Using worker: sync
[2024-06-04 22:15:05 +0530] [459678] [INFO] Booting worker with pid: 459678
/localdisk/hg/Python-Projects/venv/bin/python

^C[2024-06-04 22:15:29 +0530] [459677] [INFO] Handling signal: int
[2024-06-04 22:15:29 +0530] [459678] [INFO] Worker exiting (pid: 459678)
[2024-06-04 22:15:29 +0530] [459677] [INFO] Shutting down: Master

/localdisk/hg/Python-Projects/gunicorn-flask via 🐍 v3.11.5 (venv) took 24s 
❯ sudo gunicorn index:app
[2024-06-04 22:15:38 +0530] [459751] [INFO] Starting gunicorn 22.0.0
[2024-06-04 22:15:38 +0530] [459751] [INFO] Listening at: http://127.0.0.1:8000 (459751)
[2024-06-04 22:15:38 +0530] [459751] [INFO] Using worker: sync
[2024-06-04 22:15:38 +0530] [459752] [INFO] Booting worker with pid: 459752
/usr/bin/python
```