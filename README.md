# Python package template

This is meant to be a base for a Python package with infrastructure based on:
* [`setuptools`](https://pythonhosted.org/setuptools/setuptools.html) for
  installation
* [`setuptools_scm`](https://bitbucket.org/pypa/setuptools_scm/) for versioning
* [`tox`](https://tox.readthedocs.org/en/latest/) and
  [`py.test`](http://pytest.org/latest/) for testing
* [`flake8`](https://flake8.readthedocs.org/en/latest/) for static code
  analysis

Clone, copy everything (but the `.git` directory, of course) into your package
and make `foo` anything you want!

Remember about adjusting at least:
* `setup.py` (name, description, dependencies and classifiers)
* `setup.cfg` (`exclude` for `flake8`)
* `tox.ini` (supported Python versions)
* `.coveragerc` (name of your package)
* this `README` - cut this section out and update the rest!

# Foo

Foorther description of what is foo.

# Running tests

Run tests on all Python versions specified in `tox.ini` (2.7, 3.4 and 3.5); you
must, of course, have `tox` installed.
```bash
tox
```

If you want to use `py.test` or `flake8` directly (useful for development),
install dependencies first:
```bash
pip install -e .[tests]
```

*Note:* if you use `virtualenv` *and* have `py.test` installed system-wide, you
must re-activate this virtualenv; otherwise, system-wide `py.test` will be
used, which will most likely result in import errors.

Then you can e.g.
```bash
py.test -sv --cov
flake8
```
