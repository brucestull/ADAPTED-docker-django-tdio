# Commands and Links

## Docker Compose

- `docker compose up --build`

## DEV

```bash
docker compose -f docker-compose.yml up --build
```

```bash
docker compose exec web python manage.py  flush --no-input
```

```bash
docker compose exec web python manage.py migrate --noinput
```

```bash
docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp
```

```bash
docker compose -f docker-compose.yml down -v --remove-orphans
```


```bash
docker compose -f docker-compose.yml up --build
```

```bash
docker compose -f docker-compose.yml down
```


## PROD

```bash
docker compose -f docker-compose.prod.yml up --build
```

```bash
docker compose exec web python manage.py  flush --no-input
```

```bash
docker compose exec web python manage.py migrate --noinput
```

```bash
docker compose exec web python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp
```

```bash
docker compose exec web python manage.py collectstatic --no-input --clear
```

```bash
docker compose -f docker-compose.prod.yml down -v --remove-orphans
```


```bash
docker compose up --build
```

```bash
docker compose -f docker-compose.prod.yml up --build
```

```bash
docker compose -f docker-compose.prod.yml down
```




```bash
docker compose exec db psql --username=postgres_user_name_dev --dbname=docker_django_tdio_db_dev
```

```sql
\l
```

```sql
\c docker_django_tdio_db_dev
```

```sql
\dt
```

```sql
SELECT * FROM django_migrations;
```

```sql
SELECT * FROM accounts_customuser;
```

```sql
SELECT * FROM accounts_customuser WHERE accounts_customuser.registration_accepted = true;
```

```sql
\q
```


```bash
docker volume inspect adapted-docker-django-tdio_postgres_data
```

```bash
docker build -f ./app/Dockerfile -t config:latest ./app
```


```bash
docker compose exec web python manage.py test
```

```bash
docker compose exec web python manage.py flush --no-input
```

```bash
docker compose exec web python manage.py migrate
```


- Application Directory in Docker Container
    ![Application directory in Docker Container](../documentation_images/ApplicationLocation.png)