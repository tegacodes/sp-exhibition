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

## Folders

- Backend folder contains the python generator script (create-html) and the template files.
- Frontend folder. This is where the generated pages end up. There is also a css and page assets here.
- the html-pages is just where the html pages we develop can go. Before we configure them in the generator.

## Running the page generator

The page generator uses Jinja:

https://palletsprojects.com/p/jinja/

To run the page generator in development mode (ie. not on a pi) we want the script to read the demo data from the demo-data folder.
cd into the createHTML folder and run the python script with the DEV parameter.

```
python create_html.py DEV
```

This script will produce pages from page templates stored in the template folder.
It takes the base template code and combines with the html in each of the template files.
See this in line 88 and 89.

To add new pages, make new template files, and then add lines to this array in the create-html file to generate the pages.
