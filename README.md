
```bash
pip install virtualenv
python -m venv venv
```

```bash
source venv/bin/activate

```

```bash
pip install -e .

gunicorn --workers 3 --bind unix:my-app.sock app_exp:app
gunicorn --workers 3 app_exp:app -b 0.0.0.0:5000
gunicorn --workers 3 --worker-class eventlet app_exp:app -b 0.0.0.0:5000
gunicorn -k gevent --workers 3 --bind unix:my-app.sock app_exp:app
gunicorn --worker-class eventlet --workers 3 --bind unix:my-app.sock app_exp:app
```