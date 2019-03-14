# Flask-Boilerplate

## 1. Make a directory and cd into it. This is the project root.
```
mkdir flask-boilerplate
```

## 2. Run git init and make a .gitignore file.
```
git init
code .gitignore
https://github.com/github/gitignore/blob/master/Python.gitignore
```

## 3. Create setup.py folder with project details and dependencies.
```
code setup.py
```

## 4. Create virtual environment and activate it.
```
python3 -m venv venv
source venv/bin/activate
```
###### deactivate with 'deactivate'

## 5. Install dependencies with pip.
```
pip install -e .
pip install -e '.[test]' # developer dependencies
```
###### check dependencies with 'which (dependency)'

## 6. Set up Flask's environment variables for bash.
```
export FLASK_APP=flask_boilerplate 
export FLASK_ENV=development
```

## 7. Make your package directory and init.py file.
```
mkdir flask_boilerplate # PACKAGE MUST BE ALL LOWER CASE AND UNDERSCORE ONLY!!!!!!!
cd flask_boilerplate
code __init__.py # 2 underscores
```
###### inside __init__.py

```
from flask import Flask


def create_app():
    app = Flask(__name__)

    @app.route('/')
    def index():
        return 'Hello World!'

    return app
    
```


###### flask run command must be run from project directory, not package directory