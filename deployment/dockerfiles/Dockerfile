FROM python:3.10

ENV PYTHONUNBUFFERED=1
ENV LEVEL=PRODUCTION

WORKDIR /opt/app

# copy web app to container
COPY flatype .

# create environment, install packages
RUN python -m venv env && . env/bin/activate && \
    pip install -U pip && pip install -r src/requirements.txt && \
    python src/manage.py makemigrations