# Commands and Links

## Docker Compose

- `docker compose up --build`
- `docker compose -f docker-compose.yml up --build`
- `docker compose exec web python manage.py  flush --no-input`
- `docker compose exec web python manage.py migrate --noinput`
- `docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`

- `docker compose exec db psql --username=postgres_user_name --dbname=docker_django_tdio_db_dev`
    - `\l`
    - `\c docker_django_tdio_db_dev`
    - `\dt`
    - `SELECT * FROM django_migrations;`
    - `SELECT * FROM accounts_customuser;`
    - `SELECT * FROM accounts_customuser WHERE accounts_customuser.registration_accepted = true;`
    - `\q`
- `docker volume inspect adapted-docker-django-tdio_postgres_data`

- `docker build -f ./app/Dockerfile -t hello_django:latest ./app`

- `docker compose exec web python manage.py flush --no-input`
- `docker compose exec web python manage.py migrate`

- Application Directory in Docker Container
    ![Application directory in Docker Container](../documentation_images/ApplicationLocation.png)