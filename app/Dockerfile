# Pull official base image
FROM python:3.11.4-slim-buster

# Set working directory as /usr/src/app in Docker container
WORKDIR /usr/src/app

# Set environment variables in Docker container
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Install netcat in Docker container. Netcat is used in entrypoint.sh
RUN apt-get update && apt-get install -y netcat

# Install dependencies in Docker container
RUN pip install --upgrade pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# Copy entrypoint.sh to Docker container and make it executable
COPY ./entrypoint.sh .
RUN sed -i 's/\r$//g' /usr/src/app/entrypoint.sh
RUN chmod +x /usr/src/app/entrypoint.sh

# Copy project to Docker container
COPY . .

# Run entrypoint.sh in Docker container
ENTRYPOINT ["/usr/src/app/entrypoint.sh"]
