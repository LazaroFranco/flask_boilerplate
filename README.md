# FLASK TEMPLATE

## Installation

```
	1. $ mkdir boilerplate
	2. $ cd boilerplate
	3. $ git init
	4. $ cp ~/flask-tutorial/.gitignore .gitignore
	
	IN SETUP.PY
from setuptools import find_packages, setup

setup(
	name='boilerplate',
	version='0.0.0',
	packages=find_packages(),
	include_packages_data=True,
	zip_safe=False,
	install_requires=[
		'flask',
	],
	extras_require={
		'test': [
			'pytest',
			'coverage',
		],
	},
)
	1. $ python3 -m venv lazenv
	2. $ source lazenv/bin/activate
	3. $ pip install -e . (makes project installable, installs flask)
	4. $ pip install -e '.[test]'
	5. $ export FLASK_APP=boilerplate
	6. $ export FLASK_ENV=development
	7. $ mkdir boilerplate
	8. $ vim __init__.py
	
from flask import Flask
	
def create_app():
	app = Flask(__name__)
	
	@app.route('/')
	def index():
		return 'Hello, World'
	
	return app

	1. cd ../
        2. $ flask run
```


### RUN AFTER INSTALLATION
```
AFTER RUNNING THE INTALLATION
YOU CAN NOW OPEN YOUR APP BY ENTERING
http://127.0.0.1:5000/
```

## TESTING

```
    $ pytest

Run with coverage report::

    $ coverage run -m pytest
    $ coverage report
    $ coverage html  # open htmlcov/index.html in a browser
```
