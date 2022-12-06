# {{cookiecutter.project_name}}

## Creating a development environment

Presuming that the [pyenv](https://github.com/pyenv/pyenv) executable is available on your `$PATH`, you can create the development environment as follows:

```bash
pyenv install 3.8.10
pyenv virtualenv 3.8.10 {{cookiecutter.project_name}}
pyenv activate {{cookiecutter.project_name}}
```

[poetry](https://python-poetry.org/) is used for dependency management and is assumed to be available system-wide.

```bash
poetry install
```

### Installing pre-commit hooks

To install the pre-commit hooks, run:

```bash
pre-commit install -c .pre-commit-config.yaml
```

Pre-commit hooks can be invoked manually using:

```bash
pre-commit run -c .pre-commit-config.yaml --all-files
```

## Building the image

```bash
docker build -t {{cookiecutter.project_name}}:latest .
```

## Running the code

```bash
python -m {{cookiecutter.project_name}}
```

## Running the tests

```bash
python -m pytest .
```
