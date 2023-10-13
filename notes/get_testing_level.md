# Get Django Testing Level

1. Start the docker container

```bash
docker compose -f docker-compose.yml up --build
```

1. Use `coverage` to get the testing level

```bash
docker compose exec web coverage run manage.py test
```
