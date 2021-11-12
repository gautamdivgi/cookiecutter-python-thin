# Super thin Cookiecutter Python Project

Super thin python project. All dependencies come from the virtualenv or pyenv install python on your environment.

## Pre-requisites

- `python3`
- `pytest`
- `pip`
- `cookiecutter`
- Any packages your application needs

## Using the template

1. Create your repository. As an example we will use `https://github.com/gautamdivgi/test-cookiecutter-thin`. The project should have the `LICENSE` and `README.md` setup if needed. The template does not create it. The template provides a `.gitignore` which adds over and above the default python `.gitignore`. If you already have a `.gitignore` it will be overwritten.

2. Clone the repository locally.
```bash
git clone https://github.com/gautamdivgi/test-cookiecutter-thin
```

3. Run cookiecutter to generate the project and enter the values
```bash
cookiecutter --overwrite-if-exists https://github.com/gautamdivgi/cookiecutter-python-thin.git

full_name [John Q Public]: Gautam Divgi
email [john.q.public@github.com]: gautamdivgi@gmail.com
repo_name [Git Repo Name]: test-cookiecutter-thin
package_name [test_cookiecutter_thin]: 
project_short_description [Python Boilerplate contains all the boilerplate you need to create a Python package.]: Just testing

```

4. Test the project
```bash
[test-cookiecutter-thin] pytest tests/
=========================================================== test session starts ============================================================
platform darwin -- Python 3.9.7, pytest-6.2.5, py-1.10.0, pluggy-1.0.0
rootdir: /Users/gd9836/tmp/test-cookiecutter-thin
collected 1 item                                                                                                                           

tests/unit/test_test_cookiecutter_thin_main.py .                                                                                     [100%]

============================================================ 1 passed in 0.02s =============================================================
```

## Limitations

The limitations of this project are obviously too many to count. However, this is supposed to be a really lean project template for experiments.

## Makefile

This is a standard python makefile. All the original targets have been maintained just in case. But, the only targets that will really work are `test`, `clean`, `clean-pyc`, `clean-test`

```bash
gd9836@ILMACL02GD9836 test-cookiecutter-thin % make test
pytest
=========================================================== test session starts ============================================================
platform darwin -- Python 3.9.7, pytest-6.2.5, py-1.10.0, pluggy-1.0.0
rootdir: /Users/gd9836/tmp/test-cookiecutter-thin
collected 1 item                                                                                                                           

tests/unit/test_test_cookiecutter_thin_main.py .                                                                                     [100%]

============================================================ 1 passed in 0.02s =============================================================
gd9836@ILMACL02GD9836 test-cookiecutter-thin % make clean
rm -fr build/
rm -fr dist/
rm -fr .eggs/
find . -name '*.egg-info' -exec rm -fr {} +
find . -name '*.egg' -exec rm -f {} +
find . -name '*.pyc' -exec rm -f {} +
find . -name '*.pyo' -exec rm -f {} +
find . -name '*~' -exec rm -f {} +
find . -name '__pycache__' -exec rm -fr {} +
rm -fr .tox/
rm -f .coverage
rm -fr htmlcov/
```

