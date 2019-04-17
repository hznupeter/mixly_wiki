FROM python:3.6

RUN apt-get update && \
    apt-get install -y git mercurial texlive-full xzdec && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip install sphinx sphinx-rtd-theme PyYAML