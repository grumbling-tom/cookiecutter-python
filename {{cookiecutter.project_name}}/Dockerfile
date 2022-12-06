FROM python:3.8.10-slim

# Arbitrary working directory
WORKDIR /app/

RUN apt-get update && \
    apt-get install -y curl

# Insatll poetry system-wide
ENV POETRY_HOME="/opt/poetry"
ENV PATH="${POETRY_HOME}/bin:${PATH}"
RUN curl -sSL https://install.python-poetry.org | python -

# Install project dependencies
COPY poetry.lock pyproject.toml ./
RUN poetry config virtualenvs.create false
RUN poetry install --no-dev

# Copy source code
COPY {{cookiecutter.project_name}} {{cookiecutter.project_name}}
