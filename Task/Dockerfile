FROM python:3.9

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

COPY . requirements.txt /src
RUN pip3 install --no-cache-dir --upgrade -r /src/requirements.txt

COPY . /src
# RUN python3 /src/manage.py makemigrations
# RUN python3 /src/manage.py migrate
EXPOSE 8000

WORKDIR src

ENTRYPOINT ["/src/entrypoint.sh"]

