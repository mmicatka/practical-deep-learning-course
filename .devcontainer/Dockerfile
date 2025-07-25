FROM mcr.microsoft.com/devcontainers/python:1.1.10-3.11

COPY requirements.txt /tmp/

RUN echo "(*) Installing tools..." \
    && su - vscode -c "pip install -r /tmp/requirements.txt" \
    && apt-get update \
    && apt-get -y install --no-install-recommends graphviz

ENV PATH="/home/vscode/.local/bin:${PATH}"
