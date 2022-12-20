# cookiecutter-python

A cookiecutter providing a basic scaffolding for Python projects.

## Features

- Pre-resolved dev dependencies for linting tools such as [black](https://github.com/psf/black), [isort](https://github.com/PyCQA/isort) and [pylint](https://github.com/PyCQA/pylint)
- `.pre-commit.yaml` config for running linting regularly
- [pdoc](https://github.com/mitmproxy/pdoc) for document generation
- Basic [commitizen](https://github.com/commitizen-tools/commitizen) configuration
- Standard Python [.gitignore](https://github.com/github/gitignore/blob/main/Python.gitignore)
- Minimal Dockerfile

## Usage

You can use the cookiecutter in one of two ways; using [cruft](https://github.com/cruft/cruft):

```bash
cruft create https://github.com/grumbling-tom/cookiecutter-python
```

or using [cookiecutter](https://github.com/cookiecutter/cookiecutter):

```bash
cookiecutter https://github.com/grumbling-tom/cookiecutter-python
```
