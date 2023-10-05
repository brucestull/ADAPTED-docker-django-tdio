# pull official base image
FROM python:3.11.4-slim-buster

# set working directory as /usr/src/app in Docker container
WORKDIR /usr/src/app

# set environment variables in Docker container
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# install dependencies in Docker container
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# copy project to Docker container
COPY . .

# run entrypoint.sh in Docker container
ENTRYPOINT ["/usr/src/app/entrypoint.sh"]