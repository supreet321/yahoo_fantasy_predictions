FROM python:3.8

# Configure Poetry
ENV POETRY_VERSION=1.2.0
ENV POETRY_HOME=/opt/poetry
ENV POETRY_VENV=/opt/poetry-venv
ENV POETRY_CACHE_DIR=/opt/.cache

# Install poetry separated from system interpreter
RUN python3 -m venv $POETRY_VENV \
    && $POETRY_VENV/bin/pip install -U pip setuptools \
    && $POETRY_VENV/bin/pip install poetry==${POETRY_VERSION} --upgrade pip

# Add `poetry` to PATH
ENV PATH="${PATH}:${POETRY_VENV}/bin"

WORKDIR /api

COPY api/ /api
# Install dependencies
# COPY ./pyproject.toml ./
RUN poetry install


# Run your app
# COPY . /app
CMD ["poetry", "run",  "./manage.py", "runserver", "0.0.0.0:8000"]
