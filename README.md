# modernpython

[original post](https://medium.com/@cjolowicz/hypermodern-python-d44485d9d769)


# Install pyenv

```shell
curl https://pyenv.run | bash
```

# Instlal poetry

```shell
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
```

# Initialize your Python project using poetry init:


```
poetry init --no-interaction
```

This command will create a pyproject.toml file, the new Python package configuration file specified in PEP 517 and 518.

```
[tool.poetry.dependencies]
python = "^3.8"
```

The caret (^) in front of the version number means “up to the next major release”. 


## Creating a package in src layout

```
.
├── pyproject.toml
└── src
    └── hypermodern_python
        └── __init__.py
2 directories, 2 files
```

Use snake case for the package name hypermodern_python, as opposed to the kebab case used for the repository name hypermodern-python. In other words, name the package after your repository, replacing hyphens by underscores.

Use your own package name to avoid a name collision on PyPI.

## Managing virtual environments with Poetry

Poetry manages virtual environments for your projects. To see it in action, install the skeleton package using poetry install:

```
poetry install
```
Run a Python session inside the new virtual environment

```
poetry run pytbon

```


## Managing dependencies with Poetry

```
poetry add click

poetry update click // update
```

* The package is downloaded and installed into the virtual environment.
* The installed version is registered in the lock file poetry.lock.
* A more general version constraint is added to pyproject.toml.



