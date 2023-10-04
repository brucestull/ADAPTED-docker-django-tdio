# Commands and Links

## Docker Compose

- `docker compose up --build`
- `docker compose -f docker-compose.yml up --build`
- `docker compose exec web python manage.py migrate --noinput`
- `docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`

## Create Superusers

* `./run manage createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`
* `./run manage createsuperuser --email KnotStaff@email.app --username KnotStaff`

## Rename Project (Current Name: `doc_django`)

* `./bin/rename-project d_django_starter DDjangoStarter`

- Application Directory in Docker Container
    ![Application directory in Docker Container](../documentation_images/ApplicationLocation.png)