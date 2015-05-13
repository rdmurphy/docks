FROM python:2.7
MAINTAINER Ryan Murphy <ryan@rdmurphy.org>

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD COPY requirements /usr/src/app/requirements/

ONBUILD RUN pip install -r requirements.txt
ONBUILD RUN pip install -r requirements/local.txt

ONBUILD COPY . /usr/src/app

EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
