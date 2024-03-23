
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
gunicorn -k gevent --workers 3 --bind unix:my-app.sock app_exp:app
```