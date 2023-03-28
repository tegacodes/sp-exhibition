# sp-exhibition

## pip and virtualenv

To install third-party libraries, use virtualenv and pip. Pip allows us to easily install stuff, and virtualenv creates isolated python environments tied to specific projects.

### Getting pip/virtualenv

Your installation of Python likely comes with both, but if not, install pip by following the [instructions here](https://pip.pypa.io/en/stable/installing/). Then install virtualenv:

```
pip install virtualenv
```

You may need to run this as sudo:

```
sudo pip install virtualenv
```

### Usage

First, create a virtualenv:

```
virtualenv venv
```

This will create a folder called `venv` in your current working directory. Note: you can use whatever name you like for your virtualenv.

Next you must activate the virtualenv:

```
source venv/bin/activate
```

Then you can install packages with pip:

```
pip install packagename
```

```
For jinja:
pip install -U Jinja2
pip install requests

```

Or simply install from the requirements.txt file:

```
$ pip install -r requirements.txt
```

To run the page generator in development mode, so the script reads the demo data from the demo-data folder. cd into the createHTML folder and run:

```
python create_html.py DEV
```
