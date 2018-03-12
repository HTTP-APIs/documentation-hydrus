# documentation-hydrus
This reposity contains documentation of [hydrus](https://github.com/HTTP-APIs/hydrus) built using [Sphinx](http://www.sphinx-doc.org/en/master/#)

You can check the current documentation [here](http://hydrus.readthedocs.io/en/latest/)

### Steps to build doc

* Clone this repository.
```
$ git clone https://github.com/HTTP-APIs/documentation-hydrus.git
```

* Clone the [hydrus](https://github.com/HTTP-APIs/hydrus) repository.
```
$ git clone https://github.com/HTTP-APIs/hydrus.git
```

* It is recommended to use [virtualenv](https://virtualenv.pypa.io/en/stable/installation/) and [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/install.html) to maintain a clean environment.
```
$ source `which virtualenvwrapper.sh`
$ mkvirtualenv -p python3 hydrus
(hydrus) $ deactivate         # To deactivate the virtual environment
$ workon hydrus               # To activate virtual environment
```

* Install requirements
```
(hydrus)$ cd documentation-hydrus 
(hydrus)$ pip install -r requirements.txt
```

* Install hydrus
```
(hydrus)$ cd hydrus           # Go to your hydrus folder
(hydrus)$ pip install -e .    # To install hydrus
```

* Copy the doc folder from documentation-hydrus folder to hydrus folder (Important step).

* Everything is done now you can build the doc's .
```
(hydrus)$ cd hydrus/doc                 # The doc folder which was copied from documentation-hydrus to hydrus
(hydrus)$ sphinx-build -b html path/to/hydrus/doc/rst path/to/hydrus/doc/_build/html
```
Where "path/to/hydrus/doc/rst" and "path/to/hydrus/doc/_build/html" are your local folder path.

* To make a clean build
```
(hydrus)$ make clean
(hydrus)$ sphinx-build -b html path/to/hydrus/doc/rst path/to/hydrus/doc/_build/html
```