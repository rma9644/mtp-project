FROM mcr.microsoft.com/devcontainers/python:3.12

# Python runtime hygiene
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Create virtual environment
RUN python -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"

# Upgrade pip + build tooling (important for py3.12)
RUN pip install --upgrade pip setuptools wheel

# Install project dependencies
COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

