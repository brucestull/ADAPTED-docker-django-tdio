# Commands and Links

## Docker Compose

- `docker compose up --build`

## DEV

- `docker compose -f docker-compose.yml up --build`
- `docker compose exec web python manage.py  flush --no-input`
- `docker compose exec web python manage.py migrate --noinput`
- `docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`
- `docker compose -f docker-compose.yml down -v --remove-orphans`

- `docker compose -f docker-compose.yml up --build`
- `docker compose -f docker-compose.yml down`

## PROD

- `docker compose -f docker-compose.prod.yml up --build`
- `docker compose exec web python manage.py  flush --no-input`
- `docker compose exec web python manage.py migrate --noinput`
- `docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`
- `docker compose exec web python manage.py collectstatic --no-input --clear`
- `docker compose -f docker-compose.prod.yml down -v --remove-orphans`

- `docker compose up --build`
- `docker compose -f docker-compose.prod.yml up --build`
- `docker compose -f docker-compose.prod.yml down`



- `docker compose exec db psql --username=postgres_user_name_dev --dbname=docker_django_tdio_db_dev`
    - `\l`
    - `\c docker_django_tdio_db_dev`
    - `\dt`
    - `SELECT * FROM django_migrations;`
    - `SELECT * FROM accounts_customuser;`
    - `SELECT * FROM accounts_customuser WHERE accounts_customuser.registration_accepted = true;`
    - `\q`
- `docker volume inspect adapted-docker-django-tdio_postgres_data`

- `docker build -f ./app/Dockerfile -t config:latest ./app`

- `docker compose exec web python manage.py test`
- `docker compose exec web python manage.py flush --no-input`
- `docker compose exec web python manage.py migrate`

- Application Directory in Docker Container
    ![Application directory in Docker Container](../documentation_images/ApplicationLocation.png)