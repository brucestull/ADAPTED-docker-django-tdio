- `docker compose up --build`
- `docker compose down`
- `docker compose up`

- `docker-compose -f docker-compose.yml up -d --build`
- `docker-compose exec web python manage.py test`
- `docker-compose exec web python manage.py makemigrations`
- `docker-compose exec web python manage.py migrate`
- `docker-compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`

- `docker-compose -f docker-compose.yml up -d --build`
- `docker-compose -f docker-compose.yml down`
- `docker-compose -f docker-compose.yml up -d`

- `docker compose -f docker-compose.yml down -v --remove-orphans`

- `docker compose exec web python manage.py collectstatic --no-input --clear`
- `docker compose exec web python manage.py migrate --noinput`
- `docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`
